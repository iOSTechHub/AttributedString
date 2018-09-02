# AttributedString

[![Swift-4.0](http://img.shields.io/badge/Swift-4.0-blue.svg)]()

Super easy way to use NSMutableAttributedString


![Attributed string sample](https://res.cloudinary.com/ios/image/upload/v1535904391/AttributedString.png)

## Installation
Download source code and drag drop AttributedString folder into your project.


![Drag drop screenshot](https://res.cloudinary.com/ios/image/upload/v1535905646/AttributedString-1.png)

## Usage

### You can directly apply color, font, background color etc directly on substring or range

### Color
      let text = "This is a colorful attributed string"
      // Get NSMutableAttributedString
      let attributedText = NSMutableAttributedString.getAttributedString(fromString: text)
    
      //Apply red color on substring "This"
      attributedText.apply(color: appRedColor, subString: "This")
    
      //Apply yellow color on range
      attributedText.apply(color: appYellowColor, onRange: NSMakeRange(5, 4))


### Font

       let attributedText = NSMutableAttributedString.getAttributedString(fromString: text)
       attributedText.apply(font: UIFont.boldSystemFont(ofSize: 24), subString: "This")
       attributedText.apply(font: UIFont.italicSystemFont(ofSize: 20), subString: "string")
       
### Underline
       let text = "This is underline string"
       let attributedText = NSMutableAttributedString.getAttributedString(fromString: text)
       attributedText.underLine(subString: "This is underline string")
       
### Strikethrough and Stroke

        let text = "This is a strike and underline stroke string"
        let attributedText = NSMutableAttributedString.getAttributedString(fromString: text)
        attributedText.strikeThrough(thickness: 2, subString: "This is a")
        attributedText.applyStroke(color: appRedColor, thickness: 2, subString: "stroke string")
        
### Shadow

        let text = "This string is having a shadow"
        let attributedText = NSMutableAttributedString.getAttributedString(fromString: text)
        attributedText.applyShadow(shadowColor: .black, shadowWidth: 4.0, shadowHeigt: 4.0, shadowRadius: 4.0, subString: "This string is")
        
   ## Note:
   If string is having two same substring then use **onRange** functions instead of **subString**
   Example:  
        
        attributedText.apply(color: appYellowColor, onRange: NSMakeRange(5, 4))
        
 ### Author
 iOSTechHub, iostechhub@gmail.com
 
 ## License

Attributed is available under the MIT license. See the LICENSE file for more info.
