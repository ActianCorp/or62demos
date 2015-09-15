# or62demos Database and Presentations Release Notes

## 1.0 Welcome
Welcome to OpenROAD 6.2.0 Demos and Presentations Distribution. This readme contains information about operating system support, system requirements, installation considerations, general considerations, documentation, and contacting Actian Technical Support.

#### 1.1 Presentations in PDF format on GitHub

|Presentation|Date Given|Presenter|
|:--- | --- |:--- |
|[OpenROAD6.2NewFeatures-Overview.pdf](https://github.com/durwinwright/or62demos/blob/master/presentations/OpenROAD6.2NewFeatures-Overview.pdf)|28-May-15|[Sean Thrower](mailto:sean.thrower@actian.com)|
|[OpenROAD6 2New Client-Server and Multi-Tier Deployment.pdf](https://github.com/durwinwright/or62demos/blob/master/presentations/OpenROAD6%202New%20Client-Server%20and%20Multi-Tier%20Deployment.pdf)|11-Jun-15|[Durwin Wright](mailto:durwin.wright@actian.com)|
|[OpenROAD6.2NewFeatures-GenericMechanisms_I.pdf](https://github.com/durwinwright/or62demos/blob/master/presentations/OpenROAD6.2NewFeatures-GenericMechanisms_I.pdf)|18-Jun-15|[Sean Thrower](mailto:sean.thrower@actian.com)|
|[OpenROAD6.2NewFeatures-GenericMechanisms_II.pdf](https://github.com/durwinwright/or62demos/blob/master/presentations/OpenROAD6.2NewFeatures-GenericMechanisms_II.pdf)|25-Jun-15|[Sean Thrower](mailto:sean.thrower@actian.com)|

#### 1.2 Streaming Audio for Presentations on Youtub

  * 28th May 2015 (Sean) [**What's New in OpenROAD 6.2 Overview presentation**](https://www.youtube.com/watch?v=L74IcFCBWP8)
  * 11th June 2015 (Durwin) [**OpenROAD 6.2 - Loadnrun presentation**](https://www.youtube.com/watch?v=69ubVMOMR70)
  * 18th June 2015 (Sean) [**OpenROAD 6.2 - New Features in Detail part 1 of 2, Developers deeper dive (part 1) into new features presentation**](https://www.youtube.com/watch?v=doVw3KRXD9k)
  * 25th June 2015 (Sean) **OpenROAD 6.2 - New Features in Detail part 2 of 2, Developers deeper dive (part 2) into new features**

## 2.0 Operating System Support
OpenROAD 6.2.0 is supported on the following platforms:
* Windows Server 2008 R2 (32-bit and 64-bit)
* Windows 7 (32-bit and 64-bit)
* Windows 8 and Windows 8.1 (32-bit and 64-bit)
* Windows Server 2012 (64-bit)
Note: Microsoft Windows 95, 98, ME, NT, XP, XP Home Edition, Vista, Server 2003 (32-bit and 64-bit), 2000, and 7 Home Edition are not supported by this version of OpenROAD.

OpenROAD 6.2.0 has been exposed to the following platforms:
* Windows 10 (64-bit)
* Windows Server 2016 Technical Preview 3 (64-bit)

The Actian Product Support Lifecycle Policy determines the duration of support for OpenROAD on supported operating systems unless the operating system’s manufacturer drops support on a prior date. For the latest information about supported operating systems, visit http://supportservices.actian.com/support-services/support#lifecycle.

For complete information about all Actian products and the platforms and operating system releases they run on, see the Product Availability Matrix at http://supportservices.actian.com/support-services/support#platforms.

## 3.0 System Requirements
### 3.1 Disk Space
Disk space requirements for Windows systems are as follows:

    System Configuration      Space Required
    or562demos database       50 Mb
    Presentations             21 Mb

### 3.2 Ingres Version
This version of OpenROAD can be installed into an existing 32-bit Ingres installation, version 10.1.0 or later. All prior versions of Ingres are unsupported. This version of OpenROAD can remotely access prior versions of Ingres as well as 64-bit servers.

### 3.3 Enterprise Access Version
The unloaddb does not support Enterprise Access.  An Ingres DBMS must be used to reload the database.

## 4.0 Using reload.bat
Install the or62demos database using the reload.batscript.

To install OpenROAD

1. Before you install the or62demos database do the following
    * Create a vnode called **remotehost** that will be needed by the or62demos applications
    * Create the **remotehost::or62demkos** database
    * Confirm that the command **sql remotehost::or62demkos** can be successfully used to access the database.
    * Install the latest OR 6.2 Patch.  These demos have been tested with patch **p14811**.  This patch (or a later one can be obtained from Actian ESD).  If no patch is installed, then crashes in the OpenROAD 6.2 runtime will happen.
2. Unzip the file **openroad-6.20.15049-win-x86-p14865-a.zip** into temp directory, for example, **c:\temp**.
3. An **openroad-6.20.15049-win-x86-or62demos_install-a** directory will be created in this temp location. For example:

        c:\temp\openroad-6.20.15049-win-x86-or62demos_install-a

4. Open a Windows command window and enter the following command:

        cd c:\temp\openroad-6.20.15049-win-x86-or62demos_install-a\

5. To install OpenROAD 6.2 demos database, enter one the following command:

        reload

6. This script will create the following directory with the resources needed to run the **SetupCountyMap** component in the **D201504_ImageMapping** application in the following location,

        C:\temp\or62demos\CountyMap

7. The Presentations associated with these demos are located under the following directory

        cd c:\temp\openroad-6.20.15049-win-x86-or62demos_install-a\Presentation


If no parameter is supplied to the reload.bat script then database being reloaded will default to **remotehost::or62demos**  If a parameter is supplied to the reload.bat script then the value of that parameter contains the name of the database that will be reloaded.  It is assumed that the database exists and is accessible and updatable from the terminal monitor.

## 5.0 Contents of the remotehost::or62demos database

#### 5.0.1 The following 4GL applications are present in the or62demos database

* D201504_AllocationSystems.xml
* D201504_BitmapObjectMethods.xml
* D201504_BitmappedBkgFields.xml
* D201504_DefinedResponses.xml
* D201504_DefinedResponses_Panel.xml
* D201504_DefinedResponses_Sprites.xml
* D201504_FieldEnhancements.xml
* D201504_FrequentFlyer.xml
* D201504_FrequentFlyerGenerated.xml
* D201504_ImageMapping.xml
* D201504_OutOfBox.xml
* D201504_PropertyChanger.xml
* D201504_RUNDEMOS.xml
* D201504_ScreenCaptureTool.xml
* D201504_SpritemapConverter.xml
* D201504_Videos.xml
* D201504_VideosConverted.xml
* D201504_Videos_Old.xml

#### 5.0.2 The following is also reloaded by reload.bat

* Airline demo data that has been extended by running the *D201504_FrequentFlyer* application
* Videos data as loaded by running *demobuilder* 4GL application referenced in OR-1050
* Resource files needed to run by the *SetupCountyMap* component of the *D201504_ImageMapping* 4GL application.

### 5.1 Availability of additional demo source
The **or62demos** database is contains the Videos and Airline database tables.  It is not necessary to load this data into the or62demoks database.

#### 5.1.1 Videos Database
Demobuilder can be used to load the Videos database.  The source code for Demobuilder is available from GitHub.

#### 5.1.2 Airlines Database
The Airlines database tables can be recreated by running the following script in any Ingres DBMS instance

    %II_SYSTEM%\ingres\demo\data\recreatedemodb.bat

This script assumes that the database is called **demodb**.  Modify the script if a different database is to be loaded.

#### 5.1.3 or62demos 4GL Source Code
The source code for the 4GL source code for the or62demos applications is also available from GitHub.

## 6.0 INSTRUCTIONS Components of OR 6.2 Demo Applications
Many of the or62demos applications have an *INSTRUCTIONS* component that describes how to run each demo application.  The following section is an extract of the *INSTRUCTIONS* component located in each 4GL Application.
  * Application: **D201504_AllocationSystems**; Component: **INSTRUCTIONS**
    * **AirlineSeating**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos D201504_AllocationSystems -cAirlineSeating
                
                        Drag the "yellow" passenger to one of the available seats, and drop the
                        passenger there.
                
                        During the drag, the drag cursor "is" the yellow passenger
                        After the drop, the yellow passenger now occupies the drop seat, the
                        previous seat is now available, and a status bar message identifies the
                        new seat.
                
                        Note that each of the 300 passengers, including the yellow one, is a
                        sprite image copied and customized from the 4 sprite icons in the BgBitmap
                        Note that during the drag, the drag cursor-image is a copy of the
                        customized sprite image
                
                        Note that this drag behaviour is built into OpenROAD, and does not require
                        4GL code, although you can supply code if you want.
        
    * **AirlineSeating (code)**

                Required components:
                    none
                Required included applications:
                    none
                Other requirements:
                    none
                
                Demo:
                        w4gldev runimage workbnch.img -Tall -/appflags profile=or62demos application=allocationsystems component=airlineseating command=openscript#561
                
                        Note that the code is creating a spritedescriptor definition for each Economy
                        seat, treating it as a sector, computing each seat's size and x & y. Then the
                        code creates a sectormap from the descriptors, and stores it in the "seating plan" bitmap.
                        Go to line 265
                        Note that whenever a passenger is dragged to a new seat, the code just calls
                        the LastInputAction method, once to identify the passenger (action=
                        'mousedrag_down') and once to identify the seat (action='mousedrag_up').

  * Application: **D201504_BitmapObjectMethods**; Component: **INSTRUCTIONS**
    * **OrientBitmap**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_bitmapobjectmethods -corientbitmap
                
                        Change the reflection choice to “vertical” and click the Go button
                                The image is displayed first normally, then inverted
                        Change the reflection choice back to “none” and set the angle to around 45 and click the Go button
                                The image is displayed first normally, then at 45 degrees to normal
                        Change the backcolor to 255 (red) and click the Go button
                                The image is displayed within a red rectangle

    * **GradientBitmap**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_bitmapobjectmethods -cgradientbitmap
                        Click the Go button
                                Note that the seed image with the black outline has been used to create the gradient
                                Note that the actual seed image is tiny
                        RightClick the Go button to show a gradient arising from a text specification
                                Note that GradientBitmap will accept text specifications based on the CSS standard
                                Note that this does not (yet) include fixed-color areas or radial gradients

    * **FillBitmap**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_bitmapobjectmethods -cfillbitmap
                        Click within a county region
                                The region is filled with red
                                Note that the boundary is captured (as contiguous pixel coordinates)
                                Note that the fill can be background or boundary or wholeimage-based, exact-colour or colour-range
                        Click another county region
                                The new region is filled with red, the previous region with yellow

  * Application: **D201504_BitmappedBkgFields**; Component: **INSTRUCTIONS**
    * **BitmappedBkg_Opacity_Transparenc**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos D201504_BitmappedBkgFields -cBitmappedBkg_Opacity_Transparenc
                                Note that the frame background displays a satellite image of the world, as
                                a Mercator projection
                        Rightclick the frame
                                Note that the world image is overlaid with a field that has transparent
                                areas (forming the letters of the word "OpenROAD"), and translucent areas
                                (75% opacity).
                
                Demo:
                        w4gldev runimage workbnch.img -Tall -/appflags profile=or62demos application=d201504_bitmappedbkgfields component=bitmappedbkg_opacity_transparenc command=openscript
                                Note that the frame background displays a satellite image of the world.
                                Note that there is a buttonfield overlaying the background, but that field
                                initially is FP_CLEAR and has no text, so you cannot see it.
                        Rightclick the frame
                                Note that the code simply makes the upper field’s background transparent
                                (FP_BITMAPCLEAR) and translucent (opacity=0.75, set using the UpdBackground
                                method)

    * **BitmappedBkg_Rounding**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos D201504_BitmappedBkgFields -cBitmappedBkg_Rounding
                                Note that all these fields are identical apart from size: same bitmap, same
                                BgDisplayPolicy (BDP_CORNERED), same BgPattern (FP_BITMAPCLEAR), same
                                CornerSize (3 pixels).
                                Note that the appearance of the field, other than the text, is entirely
                                due to the bitmap, which adjusts to match the field width and height.
                                Note that whatever the field size or shape, the edges and corners are
                                preserved.
                        Click the Go button (to apply a variety of cornersizes to the fields)
                                Note that the borders are still preserved, the corners are transparent and
                                antialiased at all radii, the corners can be individually rounded.
                                Note that these borders are 2-layer concentric: OpenROAD will
                                handle borderless, 1, 2 and 3-layer concentric, gradientconcentric,
                                simple 3d, and individual-color borders.

    * **BitmappedBkg_ImageSwitch**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos D201504_BitmappedBkgFields -cBitmappedBkg_ImageSwitch
                                Note that on the left is the single bitmap (containing 10 images) that all
                                the buttons on the right use.
                                Note that initially the imageindex is unset, so all of the fields are using
                                the first image
                        Click the Go button
                                Note that each field now has a different imageindex between 1 and 10; that
                                is the only thing that has changed.

  * Application: *D201504_DefinedResponses*; Component: *INSTRUCTIONS*
    * **DecodeDefinedBehavior**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos D201504_DefinedResponses –cDecodeDefinedBehavior
                
                        Run the frame
                        Follow the instructions on the frame
                                Note that each resultant tooltiptext identifies what combination of mouse or
                                timer action and modifier key will produce what response, based on the
                                selections that were made.
                                Note that you can have multiple simultaneous responses to a single action.

  * Application: **D201504_DefinedResponses_Panel**; Component: **INSTRUCTIONS**
    * **PassportDetails**

                Required components:            none
                Required included applications: none
                Other requirements:             none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos D201504_DefinedResponses_Panel -cPassportDetails
                
                        Hover mouse over any “?” sprite
                                the infopanel frame appears alongside the sprite, displaying that
                                input field's description.
                        Move the mouse off the sprite:
                                the infopanel frame disappears.
                                Note that there is no frame code involved at all
                
                        w4gldev runimage workbench.img –Tall -/appflags profile=or62demos application=d201504_definedresponses_panel component=passportdetails, command=openscript
                                The PassPortDetails frame script contains no 4GL code
                        Hit F5 to run the edited no-code frame and mouse over the sprites
                                The infopanel frame appears and disappears as before
                                Note that there is no frame code driving this
                        Stop the running frame
                        Select the first entryfield in the edited frame
                        Click the TaggedValues entry in the Property Inspector
                                The Extended Properties dialog appears
                        Click Show all tags
                                The field's tagged values are listed
                                Note that the title and description tags contain the text that appears in
                                the infopanel
                        Click the "sprite_responses" items icon (on the right side of the table)
                                The Items dialog appears, listing a defined behavior
                                Note that the action "673" is IE_MOUSEHOVER, and it triggers the prochandle
                                for the ShowInfoPanel procedure, which is stored in a separate userclass
                                called ProceduresForRuntime@ - not in the frame. So every mousehover on
                                the "?" sprite automatically calls the ShowInfoPanel procedure.
                                No frame code is needed, just the predefined behavior.
                                Note that any number of frames can use this mechanism, without changing
                                their existing code at all.
                                Note the ShowInfoPanel procedure just looks at the triggerfield's
                                taggedvalues, copies the title into one InfoPanel field and the description
                                into another, and displays the InfoPanel frame.

  * Application: **D201504_DefinedResponses_Sprites**; Component: **INSTRUCTIONS**
    * **ProgressBars_coded**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos D201504_DefinedResponses_Sprites -cprogressbars_coded
                
                        Click the first button ("Click to count images folders")
                                The green marquee sprite zigzags continously across the top bar while
                                "images" OS folders are being searched for in an asynchronous process,
                                and stops when there are no more folders to find.
                                The number of folders found is displayed at the bottom right.
                        Click the second button ("Click to graph image types") once it activates
                                A 3-line graph is drawn showing the number of BMP, GIF and JPG files found
                                as the "images" folders are examined for image files.
                                The green progress bar grows from the left, showing the percentage of
                                folders examined so far.
                                Note that both the progress bar and the graph are painted using sprites
                                and simple code.
                                Note that the linegraph is painted on the background of the graph SubForm
                                using a sprite for each point (red sprite for BMP, blue sprite for GIF,
                                green sprite for JPG). Each line is made continuous by stretching each
                                sprite vertically where necessary; this is simple to do.

    * **ProgressBars_predefined**

                Demo:
                        w4gldev runimage workbnch.img -Tall -/appflags profile=or62demos application=d201504_definedresponses_sprites component=progressbars_coded command=openscript#520
                
                                Note the way the EventKey and Response and LoadEventBehavior methods combine to create and store a defined behavior
                        Go to line 603
                                Note that the code samples here are both setup code extracts, not needed at runtime
                                They use the InputEvent and SpriteDescriptor Helper Class methods.
                                Note that the "Compound bitmaps, sprites, animations, defined behaviors" slide shown earlier has an extract of runtime code,
                                also using the InputEvent and SpriteDescriptor Helper Class methods.
                
                Demo:
                        w4gldev runimage workbnch.img -Tall -/appflags profile=or62demos application=d201504_definedresponses component=progressbars_predefined command=open
                
                        Select the progressbar field
                        Select the TaggedValue entry in the Property Inspector
                                The Extended Properties dialog appears
                        Select the "event_responses" tag and click the right hand (Items) icon
                                The TaggedValue Items dialog appears
                        Rightclick the node beginning "999"
                                The Tooltiptext window displays a description of the defined behaviour
                                stored as this item:
                                - the trigger is a timer alert (999=IE_TICKPOINT)
                                - the field changed will be this field (progressbar)
                                - the response is to paint three sprites onto the field, one of which is
                                  the actual green progress bar
                                Note that there are 100 responses defined, differing only the in the width
                                (between 1% and 100%) of the "progress" sprite (the first one in the
                                spritemap shown). Only one of these possible responses is painted each
                                time; which one is defined by an index which the demo's 4GL processing
                                supplies when it triggers the behaviour; the value of that index is the
                                "progress" being measured, computed as a percentage.
                                            
    * **GlobeNightShadow**

                        w4gldev rundbapp remotehost::or62demos D201504_DefinedResponses_Sprites -cglobenightshadow
                
                        The night shadow moves slowly right to left. The moon rises and moves more
                        quickly right to left, initially over the shadow, later not.

  * Application: **D201504_FieldEnhancements**; Component: **INSTRUCTIONS**
    * **TreeViewFieldChanges**

                Required components:
                        none
                Required included applications:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_fieldenhancements -ctreeviewfieldchanges
                        Click the top button to populate the tree with nodes representing folders
                                Note the checkboxes, FullRowSelect highlight, customized nodeheight and inset
                        Holding down the Shift button, Drag the "Development" node onto the "ST" node
                                Note that the node is inserted at that location
                        Drag the "Development" node onto the "Tools" node
                                Note that the node is attached to that node
                        Click the second button to populate the tree with nodes representing files
                                Note the individual-node font control, background control
                        RightClick an unselected node
                                Note the focus switches to the node while the dropdown is visible
                        Click whitespace to release the dropdown
                                Note the focus switches back to the previously-selected node node

    * **TabFolderBitmappedTabs**

                Required components:
                        none
                Required database:
                        none
                Required included applications:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_fieldenhancements -ctabfolderbitmappedtabs
                                - The tabfolder initially displays rectangular bitmapped tabs
                        Click each tab in turn
                                Note the tab highighted text and the page display
                                Note that the tabbar can now (6.2) be coloured or clear

    * **BDPTabHighlighting**

                Required components:
                        none
                Required database:
                        none
                Required included applications:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_fieldenhancements -cbdptabhighlighting
                                - The tabfolder displays gradiented bitmapped tabs
                        Click the "Add tab bitmaps" button
                                - The unselected tabs display a bordered double-gradient bitmapped-background
                        Select different tabs to confirm this
                        Click the "Add highlighting" button
                        Mouse across the unselected tabs
                                - The moused tab highlights during mouseover
                        Mouse across the selected tab
                                - The moused tab does not highlight
                                Note that this is the characteristic Windows7 behaviour for tabfolders

    * **TableFieldExactWidth**

                Required components:
                        none
                Required database:
                        remotehost::demodb      (the OpenROAD-specific extended version)
                Required included applications:
                        D201504_frequentflyergenerated
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_fieldenhancements -ctablefieldexactwidth
                        Click second toolbar icon ("Open dataset")
                        Type 27 in the "record" field and hit return
                                - JFK airport details will display
                        Select each tab in turn
                                - 4 of these are tablefields, each of different default width, but
                                  all showing the same displayed width, providing a clean display

    * **SubFormSizeToFit**

                Required components:
                        none
                Required database:
                        none
                Required included applications:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_fieldenhancements -csubformsizetofit
                                - Note the top toolbar help button, already right-aligned within
                                  a subform that has SizeToFit = STF_FRAMEHORIZONTAL
                        Click the ApplySizeToFit button to make the pink subform STF_PARENT
                                - Note the pink subform fills its parent to the right and bottom
                        Resize the frame from the right to truncate the pink subform and make
                        the help button disappear
                        Click the ApplySizeToFit button again to make the pink subform STF_FRAME
                                Note that the pink subform has resized to align with the frame (the
                                help button has reappeared)

    * **SubFormChildMargins**

                Required components:
                        none
                Required database:
                        none
                Required included applications:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_fieldenhancements -csubformchildmargins
                        Click the help button on the pink subform to apply a top and right margin
                        to the subform
                                - Note that the help button is inset 3 pixels
                        Click the ApplySizeToFit button twice to make the pink subform STF_FRAME
                                - Note the help button is inset by the same amount in the resized
                                  pink subform
                        Resize the frame from the right to resize the pink subform
                                - Note the help button is still inset by the same amount in the
                                  resized pink subform
                        Click the help button repeatedly on the pink subform to increase the
                        margins by 3 pixels each time
                        Resize the frame from the right to resize the pink subform, repeatedly
                                - Note the help button inset is always honoured

    * **ControlButtons**

                Required components:
                        none
                Required database:
                        none
                Required included applications:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_fieldenhancements -ccontrolbuttons
                                - The four tablefields each display a different controlbutton
                        Click each controlbutton in turn to show the menu (click any option to close the menu)
                                Note that the first controlbutton is the original image, honouring the FgColor and BgColor
                                Note that the third and fourth controlbuttons are identical images, honouring the FgColor and BgColor

    * **EntryFieldInnerMargins**

                Required components:
                        none
                Required database:
                        none
                Required included applications:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_fieldenhancements -centryfieldinnermargins
                                - Note that in each row the fields increase in cornerradius going right
                                  (0px, 5px, 10px, 15px)
                        Tab into each entryfield of the top row, pausing on the third one
                                - Note that all the fields in this row have margins of 2 pixels
                                - Note that in the third field (which has 10px corner radius), the
                                  corners of the text highlight rectangle appear outside the rounded
                                  corners of the entryfield, an unacceptable effect
                        Tab into each entryfield of the bottom row
                                - Note that these fields increase in left and right margin going right
                                  (2px, 4px, 6px, 8px)
                                - Note that in every field, the corners of the text highlight
                                  rectangle appear within the rounded corners of the entryfield,
                                  an acceptable effect, because of the increasing margins

  * Application: **D201504_FrequentFlyer**; Component: **INSTRUCTIONS**
    * **Userclass Generation**

                Required vnode:
                        remotehost
                Required database (accessible using vnode):
                        Ingres demodb database, extended using ExtendDemodbDatabase
                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev runimage workbench.img -Tall -/appflags profile=or62demos application=d201504_frequentflyer
                
                        Create and edit a userclass called User_profile
                        Choose Attributes | Insert | From Database Table
                                The Select a Database Table dialog appears
                        Click the "List Tables ..." button
                                The Table Selection dialog appears
                        Select the "user_profile" table and click OK
                        Tick the Trim prefix.. , the Capitalize .., and the Cascade.. options
                        Type "up_" as the prefix to trim
                        Click OK to start the generation process
                        Select "Yes to All" whenever a confirmation popup appears
                        Allow the generation to run to completion (the trace window stops adding new
                        lines)
                                The User_profile attributes table will list:
                                - attributes corresponding to each column in the user_profile database table
                                - two additional attributes (airport and flights) corresponding to tables
                                  with which the user_profile table has a key-based relationship
                                The Workbench Components panel will list:
                                - the user_profile userclass that you created initially
                                - 5 additional userclasses that have been automatically created (by the
                                  cascade facility), including the airport and flight userclasses needed
                                  as the datatypes of the relationship-derived attributes
                                 and
                                Note that the userclass's Queries attribute has also been populated with
                                fully-instantiated QueryObjects able to populate the business objects from
                                the database and accept changes, deletions and new records, and to list
                                business objects for the enduser to choose.

    * **Display Generation**

                Required vnode:
                        remotehost
                Required database (accessible using vnode):
                        Ingres demodb database, extended using ExtendDemodbDatabase
                Required components:
                        The userclasses created using the Userclass Generation demo:
                        - applying the userclass generator on remotehost::demodb, using user_profile
                          as the seed userclass.
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev runimage workbench.img -Tall -/appflags profile=or62demos application=d201504_frequentflyer
                
                        Create and edit User_profileDetails frame from the active_display frametemplate
                        Choose Insert | Display from User Class
                                The Select a User Class dialog appears
                        Select d201504_frequentflyer from the Application list
                        Select user_profile from the User Class list
                                Note that there are rich Advanced and Customize options to tune the
                                choice of fields to display, their properties, and the overall layout,
                                and which capabilities to include (interframe navigation, for example)
                        Click OK and wait for the display to be generated
                                The generated frame shows the userclass attributes as fields, grouped
                                into panels by their category (identity fields, location fields, contact
                                fields, etc), with object panels on the right hand side (Airport).
                                Tablefields are at the bottom, as pages of a tabfolder (most business objects
                                in the real world have several array attributes, not just one or none).
                                Field order is preserved, so that name fields and address fields are in
                                the right order.
                                The size of the frame is as close as possible to whatever size you
                                gave the Frame Editor.
                        Hit F5 to run the frame
                        Rightclick the Open (second) toolbar icon and choose the Selected Item option
                        Doubleclick the sample@ingres.com entry
                                The corresponding user is displayed
                                Note that the frame can be edited and the changes saved
                        Leftclick the Open (second) toolbar icon
                                All the users are selected, and the first one displayed
                        Click the Next (ninth, right-arrow) toolbar icon repeatedly
                                Each user in the set is displayed in turn
                        Click the Menu icon in the topright of the Airport panel and choose the Open
                        option
                                The generated Airport frame is displayed, populated with the airport
                                details, including the lists of arrivals and departures, both the scheduled
                                ones and the actual flights this user has taken
                                Note that the generation process is completely generic - you would need
                                to change the Airport frame tabs to Flight Arrivals, Flight Departures
                                Scheduled Arrivals, Scheduled Departures.

    * **Create demodb database (without extension)**

                /*
                **      Create demodb database (without extension)
                **
                **      Note: If you only have vnode access to the installation, you are unlikely to
                **      have II_SYSTEM\ingres\demo\data, which contains the demodb data and the
                **      recreatedemodb.bat file.
                **      Even if you do have the data folder, you will need to edit the bat file and
                **      probably the copy.in to prefix the database name with the vnode
                */
                        Open the Ingres command window for the installation that the remotehost vnode
                        points to
                        >cd data
                        >recreatedemodb.bat >demodb.log
                                Any existing demodb database will be dropped
                                The demodb database will be created in the installation and populated.
                        >edit demodb.log
                                Any errors will be logged. If there are errors, correct the problem and
                                rerun recreatedemodb.bat

    * **Extend demodb database for use with OpenROAD 6.2**

                /*
                **      Extend demodb database for use with OpenROAD 6.2
                */
                        w4gldev rundbapp remotehost::or62demos d201504_frequentflyer -cextenddemodbdatabase
                
                        Click the "Extend DemoDb" button
                                All the required additional tables, data and metadata will be added to
                                the demodb database

    * **Revert demodb database for use with OpenROAD 6.2**

                /*
                **      Revert demodb database to the initial (Ingres) version
                */
                        w4gldev rundbapp remotehost::or62demos d201504_frequentflyer -cextenddemodbdatabase
                
                        Click the "Revert DemoDb" button
                                All the tables, data and metadata added to demodb by the "Extend DemoDb"
                                option will be removed

  * Application: **D201504_FrequentFlyerGenerated**; Component: **INSTRUCTIONS**
    * **New user_profile based frame**

                Required data database:
                        remotehost::demodb (extended for OpenROAD)
                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev runimage workbnch.img -Tall -/appflags profile=or62demos application=d201504_frequentflyergenerated
                        Create a new frame User_profileDetails2 using the active_display template
                        Choose Insert | Display from User Class
                        Select the "d201504_frequentflyergenerated" application and "user_details" user class
                        Click "Customize" to display the relevant dialog
                        Select the "Email" node in the left hand tree
                                The email attribute's extended properties are displayed
                                Note that this Customize dialog provides a way to override the generated
                                userclass settings either temporarily or permanently. Typical changes are
                                to mark some attributes as never displayed, or to correct the allocated
                                category or subtype of an attribute.
                                Note that the temporary overrides can be saved and subsequently reused as
                                named customizations
                        Select other nodes in the left hand tree
                                The corresponding extended properties are displayed
                                Note that these differ, depending on whether the attribute is of object type

  * Application: **D201504_ImageMapping**; Component: **INSTRUCTIONS**
    * **CountyMap - Facility**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev runimage workbench.img -Tall -/appflags profile=or62demos application=D201504_ImageMapping component=countymap command=open
                
                        Select the SetupName entry in the Property Inspector
                                The Setup Frame dialog will appear
                        Select the "D201504_ImageMapping" application and the "setupcountymap" frame,
                        and click OK
                                The SetupCountyMap setup frame will run
                        Click the "County Outlines" tab
                                An outline map of English counties will appear
                        Click the "Setup the county map" button
                                After a few seconds each county will be coloured a different shade of grey
                        Close the setup frame
                                Note that the setupframe has analysed the data it has and has setup the
                                CountyMap frame to run whenever the enduser needs it.
                        Run the CountyMap frame
                        Click any point in SouthEast England on the satellite image
                                The county under the mouse is outlined in green, the name and demographic
                                data for that county appear on the right, and a satellite image of that
                                county appears above the data
                        Click outher points in SouthEast England to show different counties and their
                        data
                                Note that this is a genuinely useful facility, presenting genuinely useful
                                data, using a simple generic mechanism adaptable to a wide range of
                                business cases.
                
                        Select CountyMap, then choose File | Revert to last saved
        
    * **CountyMap - Mechanism**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev runimage workbench.img -Tall -/appflags profile=or62demos application=D201504_ImageMapping component=countymap command=open
                                The CountyMap frame is opened for edit
                                Note that the satellite map is a low-resolution placeholder, and the frame
                                contains only runtime code, no setup code
                        Select the SetupName entry in the Property Inspector
                                The Setup Frame dialog will appear
                        Select the "D201504_ImageMapping" application and the "setupcountymap" frame,
                        and click OK
                                The SetupCountyMap setup frame will run
                                Note that the displayed satellite image in the setup frame is the
                                full-resolution version, which will be copied to the target frame.
                        Click the County Populations tab
                                The county demographic data is displayed
                                Note that this is the business data the enduser wants to see (any other
                                data would work just as well - crime statistics, for example)
                        Click the "County Outlines" tab
                                An outline map of English counties appears
                                Note that such region outline maps are freely available for almost any
                                type of region: country, parish, sales area, land-ownership, pie chart ...
                        Click the Postcode Locations tab
                                A table of postcodes with geographical location, town and county is displayed
                                Note that this plus the outline map gives everything needed to build our
                                map-based application - no need at all for expensive GEO data in such cases
                        Click the "Setup the county map" button
                                After a few seconds each county will have a unique colour
                                Note that the shades uniquely identify the different counties:
                                - for each county used a postcode to locate the corresponding pixel
                                  in the outline map; then used the FillBitmap method to colour the county
                                  uniquely and to capture the county's boundary coordinates (the set of
                                  pixels that will completely enclose the county).
                        Close the setup frame
                                Note that we could now just save and close the CountyMap frame; from now
                                on it is ready to run [dont do this though, as the demo is likely reused]
                        Run the CountyMap frame
                        Click any point in SouthEast England on the satellite image
                                The county under the mouse is outlined in green, the name and demographic
                                data for that county appear on the right, and a satellite image of that
                                county appears above the data
                                Note that when the enduser clicked on the satellite map, we got the
                                  corresponding pixel from our coloured map, we used the unique pixel
                                  colour to identify the county, we use the county name to get the
                                  demographic data, we use the boundary coordinates to extract the
                                  satellite image of the county from the main satellite image.
                
                        Select CountyMap, then choose File | Revert to last saved

    * **CountyMap - Using Setup**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev runimage workbench.img -Tall -/appflags profile=or62demos application=D201504_ImageMapping component=countymap command=open
                                The CountyMap frame is opened for edit
                        Select the SetupName entry in the Property Inspector
                                The Setup Frame dialog will appear
                        Select the "D201504_ImageMapping" application and the "setupcountymap" frame,
                        and click OK
                                The SetupCountyMap setup frame will run
                        Click the "County Outlines" tab
                                An outline map of English counties will appear
                        Click the "Setup the county map" button
                                After a few seconds each county will be coloured a different shade of grey
                                Note that the CountyMap frame, the one that the enduser will see at
                                runtime, has been setup and ready to go:
                                - the grey (mask) image, the county boundary coordinates, and the
                                  cross-reference of these to the county demographic data, have all been
                                  generated by the setup frame, and applied to the CountyMap frame
                        Close the setup frame
                        Run the county map frame
                        Click any point in SouthEast England on the satellite image to confirm that
                        setup has worked correctly
                                - the county under the mouse is outlined in green, the name and demographic
                                  data for that county appear on the right, and a satellite image of that
                                  county appears above the data
                
                        Select CountyMap, then choose File | Revert to last saved

  * Application: **D201504_OutOfBox**; Component: **INSTRUCTIONS**
    * **New Frame AirportMaintenance**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev runimage workbench.img -Tall -/appflags profile=or62demos application=D201504_OutOfBox
                
                        Create frame AirportMaintenance using table_editor template
                                A table-selection dialog appears
                        Specify “airport” table from the table list and click OK
                                A tablefield-based display is created, whose columns correspond to the
                                airport table’s columns
                        Save the frame
                        Run the frame
                        Choose File | Open
                                The table populates with all the data from the database airport table
                        Select one or many records
                                Selected records have red text, and the current row is marked with
                                a red asterisk
                        Scroll the data
                        Insert a row (using the File menu or the toolbar icons)
                        Type new data into the added row
                        Save the new record
                        Close and reopen the frame and choose File | Open and scroll if necessary to
                        confirm that the record you created is in the database
                                The added record is there
                        Delete the record and save
                        Close and reopen the frame and choose File | Open and scroll if necessary to
                        confirm that the record you deleted is no longer in the database
                                The added record is gone
                
                Cleanup:
                        Delete the frame you created

  * Application: **D201504_OutOfBox**; Component: **INSTRUCTIONS**
    * **New Frame AirportMaintenance**

                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev runimage workbench.img -Tall -/appflags profile=or62demos application=D201504_OutOfBox
                
                        Create frame AirportMaintenance using table_editor template
                                A table-selection dialog appears
                        Specify “airport” table from the table list and click OK
                                A tablefield-based display is created, whose columns correspond to the
                                airport table’s columns
                        Save the frame
                        Run the frame
                        Choose File | Open
                                The table populates with all the data from the database airport table
                        Select one or many records
                                Selected records have red text, and the current row is marked with
                                a red asterisk
                        Scroll the data
                        Insert a row (using the File menu or the toolbar icons)
                        Type new data into the added row
                        Save the new record
                        Close and reopen the frame and choose File | Open and scroll if necessary to
                        confirm that the record you created is in the database
                                The added record is there
                        Delete the record and save
                        Close and reopen the frame and choose File | Open and scroll if necessary to
                        confirm that the record you deleted is no longer in the database
                                The added record is gone
                
                Cleanup:
                        Delete the frame you created

  * Application: **D201504_PropertyChanger**; Component: **INSTRUCTIONS**
    * **W7styler**

                Required vnode:
                        remotehost
                Required database (accessible using vnode):
                        Ingres demodb database, extended using ExtendDemodbDatabase
                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos propertychanger –cw7styler
                        Default all options except application (choose D201504_VIDEOS)
                                Note that the conversion takes around 2 minutes for the Videos application
                                (around 30 frames)
                        Compare the restyled application with the old (_BAK) version:
                                w4gldev rundbapp remotehost::or62demos D201504_VIDEOS_BAK
                                w4gldev rundbapp remotehost::or62demos D201504_VIDEOS
                
                        Use Ctrl-Tab to move the inputfocus onto the buttonfields to show pulsing.
                        Mouse over the buttonfields and tablefield headers to show highlighting.

  * Application: **D201504_RUNDEMOS**; Component: **INSTRUCTIONS**
    * **Requirements**

                Required database name for repository database:
                        or62demos
                Required database name for demo data database:
                        demodb (containing the Ingres demo data, extended for OpenROAD)
                Required vnode name:
                        remotehost
                Required Workbench profile name:
                        or62demos

    * **RunDemos_I**

                /*
                **      RunDemos_I
                */
                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        Powerpoint presentation OpenROAD6.2NewFeatures-Overview.pptx
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_rundemos -crundemos_I
                                - Note that a transparent "list" of numbered toggles will display.
                                  Some numbers will be suffixed with .1, .2 etc.
                        Whenever the presentation reaches a demo page (one whose page number
                        corresponds to a toggle number),
                                hit the "b" key to blank the presentation
                                tick that toggle to start the demo.
                        When the demo is complete,
                                close the demo (for Workbench demos, be sure to close Workbench itself)
                                hit the "b" key to redisplay the presentation.

    * **RunDemos_II**

                /*
                **      RunDemos_II
                */
                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        Powerpoint presentation OpenROAD6.2NewFeatures-GenericMechanisms_I.pptx
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_rundemos -crundemos_II
                                - Note that a transparent "list" of numbered toggles will display.
                                  Some numbers will be suffixed with .1, .2 etc.
                        Whenever the presentation reaches a demo page (one whose page number
                        corresponds to a toggle number),
                                hit the "b" key to blank the presentation
                                tick that toggle to start the demo.
                        When the demo is complete,
                                close the demo (for Workbench demos, be sure to close Workbench itself)
                                hit the "b" key to redisplay the presentation.

    * **RunDemos_III**

                /*
                **      RunDemos_III
                */
                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        Powerpoint presentation OpenROAD6.2NewFeatures-GenericMechanisms_II.pptx
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_rundemos -crundemos_III
                                - Note that a transparent "list" of numbered toggles will display.
                                  Some numbers will be suffixed with .1, .2 etc.
                        Whenever the presentation reaches a demo page (one whose page number
                        corresponds to a toggle number),
                                hit the "b" key to blank the presentation
                                tick that toggle to start the demo.
                        When the demo is complete,
                                close the demo (for Workbench demos, be sure to close Workbench itself)
                                hit the "b" key to redisplay the presentation.

  * Application: **D201504_ScreenCaptureTool**; Component: **INSTRUCTIONS**
    * **ScreenCapture**

                /*
                **      ScreenCapture
                */
                Required components:
                        none
                Required included applications:
                        none
                Other requirements:
                        none
                
                Demo:
                        w4gldev rundbapp remotehost::or62demos d201504_screencapturetool -cscreencapture
                
                        Drag the capture window to the location to be captured
                        Resize (and reposition) the capture window until it displays the exact area to be
                        captured
                        Click the Capture button
                                The captured area appears as a thumbnail in the frame
                        Click the Save as … button
                                The File Save dialog appears
                        Choose or enter a folder and a “bmp” frame name to write the captured image out
                        as, and click Save
                                The image is written to file, and the File Save dialog disappears
                        RightClick the Save as … button
                                The image from the file is displayed in the centre of the screen
                                Note that the file image is identical to the captured area (except that
                                that may be greyed, depending on the utility displaying the file image)

  * Application: **D201504_SpritemapConverter**; Component: **SpritemapConverter**

                Paste or type the spritemap text into the spritemap panel and click the button to see the detailed definition in the
                spritedescriptor panel.
                If you have multiple specifications in the spritemap, the one the text cursor is currently on will be displayed.
                If you change the descriptor details, and click the button, the corresponding spritemap will be displayed.

 * Application: **D201504_Videos**; Component: **main_control**

                Original Videos application

  * Application: **D201504_Videos_Old**; Component: **main_control**

                Original Videos application

  * Application: **D201504_VideosConverted**; Component: **main_control**

                Converted Videos application updated by Property Changer to Windows 7 Styling.


## 7.0 Documentation
You can find the latest updates to the OpenROAD documentation set online at [Actian Home](http://docs.actian.com). The documentation set is provided in Adobe Portable Document Format (PDF) at http://esd.actian.com. The PDF documentation is no longer included with the main installer.

Changes to the documentation are highlighted in "Documentation Updates" in the OpenROAD 6.2.0 Release Summary.

## 8.0 Your Support Options
Enterprise customers with active maintenance and support contracts have full access to Actian Support, including online use of our case management system and knowledge base, at the [Customer Portal](https://support.actian.com).

If you have an active support contract and want to register for access to the Customer Portal, use the enrollment form at [Actian Customer Portal Registration](http://supportservices.actian.com/user/register.php). (Your Account Number ID is required.)

If you do not have a support agreement for Actian Corporation products and are interested in purchasing support, contact us at sales@actian.com.

For more information about support options, visit [Actian Support Options](http://supportservices.actian.com/support-services/support).

Free support is available from the Actian Open Source Community. Community members may obtain assistance for Actian Corporation products by registering with the Actian Community Site and using the available tools. To register, go to [Actian Open Source Community](http://supportservices.actian.com/community)  and click Register.
