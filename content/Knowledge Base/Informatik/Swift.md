

### Bedingte Anweisungen

- If-Anweisung Bedingung hinzufügen (true)
- Else-Anweisung (false)
- **Boolescher Wert:**
    - Eine Kondition ist immer entweder **true** oder **false**
    - Boolesche Werte mit bedingten Anweisungen, um einem Programm zu sagen, wann bestimmte Codeblöcke ausgeführt werden sollen

### logische Operatoren

- Operator
    
    - Symbol, das eine Aktion repräsentiert
    - **AND &&**
        - wenn alle Bedingungen erfüllt
    - **OR ||**
        - mindestens eine Bedingung erfüllt
    - **NOT !**
        - Gegenteil erfüllt (false → true)
- App-development basics: camera
    
    - components
        
        - a component is a building block - such as a space or a camera - used in building an app
        - starts by creating an instance
    - components Code
        
        // Create the space.
        
        **let** space = Space()
        
        // Create the component.
        
        **let** camera = SwiftyCamera(style: .plain)
        
        // Add the component to the space.
        
        space.add(camera, at: Point(x: 0, y: 0), size: Size(width: 500, height: 500))
        
        // Start the camera.
        
        camera.start()
        
    - instance
        
        - value of a particular type
        - in let motion = MotionSensor()
            - motion is an instance of type MotionSensor
    - space
        
        - container component into which components can be put into
        - empty canvas on which components you can start laying out components
    - SwiftyCamera
        
        - component, that can be used to take fotos using the front or rear camera on iPad
    - property
        
        - variable (a named container that stores a value) defined inside a type
        - used to change the appearance and behavior of component has its own set of properties
    - type
        
        - named grouping of properties (the features) and methods (the behaviors) of kind of data
    - literal
        
        - gives the ability to embed an image or color directly into code using the image library or color picker
        - actual values of data represented in their native format, directly within the editor
    - seeing your photos
        
        - image view component
        - allows image to be viewed such as a photo
        - connecting image view to camera → photo taken can be seen
    - seeing your photos Code
        
        // Create the space
        
        **let** space = Space()
        
        // Create the components.
        
        **let** camera = SwiftyCamera(style: .plain)
        
        **let** imageView = ImageView()
        
        **let** albumView = PhotoAlbumView()
        
        // Add the components to the space.
        
        space.add(camera, at: Point(x: 0, y: -175))
        
        space.add(imageView, at: Point(x: 0, y: 120), size: Size(width: 480, height: 250))
        
        space.add(albumView, at: Point(x: 0, y: 375), size: Size(width: 480, height: 200))
        
        // Start the camera.
        
        camera.start()
        
        // Set the properties of the image view.
        
        imageView.borderColor =  colorLiteral(red: 0.721568644, green: 0.8862745166, blue: 0.5921568871, alpha: 1)
        
        imageView.backgroundColor =  colorLiteral(red: 0.721568644, green: 0.8862745166, blue: 0.5921568871, alpha: 1)
        
        imageView.borderWidth = 20
        
        imageView.cornerRadius = 20
        
        // Open your photo album.
        
        **let** myAlbum = PhotoAlbum(named: "Learning Coding Apps with Swift")
        
        albumView.album = myAlbum
        
        // Connect the camera to the image view.
        
        camera.photoTaken.connect(to: imageView.input)
        
        // Connect the camera to the album view.
        
        camera.photoTaken.connect(to:albumView.imageInput)
        
    - build a photo board Code
        
        **let** space = Space()
        
        space.backgroundImage =  imageLiteral(resourceName: "cf_bulletinboard-bkg.png")
        
        // Open your photo album.
        
        **let** myAlbum = PhotoAlbum(named: "Learning Coding Apps with Swift")
        
        // Add photos.
        
        **let** picture1 = ImageView()
        
        picture1.image = myAlbum[0].image
        
        space.add(picture1, at: Point(x: -200, y: 300), size: Size(width: 300, height: 300))
        
        // Add stickers and picture frames.
        
        **let** sticker1 = ImageView()
        
        sticker1.image =  imageLiteral(resourceName: "cf_ccBuildingaCamera004.png")
        
        space.add(sticker1, at: Point(x: -200, y: 420), size: Size(width: 200, height: 200))
        
        **let** frame1 = ImageView()
        
        frame1.image =  imageLiteral(resourceName: "cf_cloud-mask.png")
        
        space.add(frame1, at: Point(x: 100, y: -100), size: Size(width: 400, height: 400))
        
        // Style your stickers and picture frames.
        
        space.add(sticker1, at: picture1.position, size: Size(width: 300, height: 300))
        
        picture1.borderColor =  colorLiteral(red: 0.8, green: 0.1, blue: 0.1, alpha: 1)
        
        picture1.borderWidth = 15
        
        sticker1.rotation = 5
        
        frame1.scale = 2.0
        
        picture1.cornerRadius = 10
        
        sticker1.alpha = 0.5
        
        // Add labels.
        
        **let** label = Label()
        
        label.text = "test"
        
        space.add(label, at: Point(x: -20, y: 200))
        
        // Style your labels.
        
        **let** style = TextStyle(.Copperplate, fontSize: 50, color:   colorLiteral(red: 0.572549045085907, green: 0.0, blue: 0.23137255012989044, alpha: 1.0))
        
        label.textStyle = style
        
        label.rotation = 90.0
        
        label.scale = 2.0
        
        label.shadowColor =  colorLiteral(red: 0.9372549057006836, green: 0.3490196168422699, blue: 0.1921568661928177, alpha: 1.0)
        
        label.shadowOffset = Size(width: 1.5, height: 1.5)
        
- Eine Funktion generalisieren
    
    ```swift
    var gemCounter = 0
    var lockCounter = 0
    
    func experTurnAround() {
        expert.turnLeft()
        expert.turnLeft()
    }
    func LockUp() {
        expert.turnLockUp()
        experTurnAround()
        expert.turnLockUp()   
        lockCounter += 1
    }
    func LockDown() {
        expert.turnLockDown()
        experTurnAround()
        expert.turnLockDown()    
        lockCounter -= 1
    }
    
    func resetLock() {
        while lockCounter != 0 {
            LockDown()        
        }
    }
    while gemCounter != 3 {
        if character.isOnGem {
            character.collectGem()
            gemCounter += 1
            character.turnLeft()
            character.turnLeft()
            character.moveForward()
            resetLock()        
        }
        if !character.isBlockedLeft && gemCounter == 1 {
            character.turnLeft()
            character.moveForward()
            character.turnRight()
        }
        if character.isBlocked {
            LockUp()        
        }
        else {
            character.moveForward()
        }
    }
    ```