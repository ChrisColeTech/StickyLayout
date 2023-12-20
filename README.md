# StickyLayout 
[![codecov](https://codecov.io/gh/jeffreysfllo24/StickyLayout/branch/master/graph/badge.svg)](https://codecov.io/gh/jeffreysfllo24/StickyLayout)
[![pod](https://cocoapod-badges.herokuapp.com/v/StickyLayout/badge.png)](https://cocoapods.org/pods/StickyLayout)
[![Badge w/ Platform](https://cocoapod-badges.herokuapp.com/p/StickyLayout/badge.svg)](https://cocoadocs.org/pods/StickyLayout)
![License MIT](https://go-shields.herokuapp.com/license-MIT-blue.png)

# New 2023 Update  
- [X] Added Fixed Footers option
- [X] Fixed footer will stick to the bottom of the screen, even when there are not enough sections to fill the screen.

## Dynamically Set `fixedFooter` Property

To dynamically set the `fixedFooter` property in your app, you can modify the property value based on some condition or user interaction. Below is an example of how you might toggle the `fixedFooter` property:

```
// Assume you have a reference to your custom layout
let customLayout = DSCStickyLayout(stickyConfig: yourStickyConfig)

// Dynamically set `fixedFooter` based on some condition or user interaction
customLayout.fixedFooter = shouldUseFixedFooter // Replace `shouldUseFixedFooter` with your actual condition

// Assign the custom layout to your collection view
yourCollectionView.collectionViewLayout = customLayout

// Call reloadData on your collection view to apply the changes
yourCollectionView.reloadData()
```

Example:
 <p float="right">
    <img src="Art/FixedFooter_2023.gif" float="right">
  </p>

  ## Usage:
 
<p>
  <p float="left">
    <img src="Art/StickyLayout_Calendar.gif" float="top">
    <img src="Art/StickyLayout_swimming.gif" float="bottom">
  </p>

  <p float="right">
    <img src="https://github.com/jeffreysfllo24/StickyLayout/blob/master/Art/StickLayout_Tabular.gif" float="right">
  </p>
</p>

##### The above examples are accessible in the `example` folder.

## What is StickyLayout?
**StickyLayout** is a collection view layout that provides sticky row and column configurability.

## Features

- [X] Configurable Sticky options.
- [X] Pure Swift 5.
- [X] Horizontal and vertical scrolling support.
- [X] Row spacing and column spacing support.
- [X] Works with every `UICollectionView`.

## Setup
Using **StickyLayout** quick and simple. First import `StickyLayout`.

```swift
import StickyLayout
```

You then have the option of creating an instance of `StickyConfig`, where you can specify which rows/columns you want to be sticky.

```swift
let stickyConfig = StickyLayoutConfig(stickyRowsFromTop: 1,
                                stickyRowsFromBottom: 0,
                                stickyColsFromLeft: 1,
                                stickyColsFromRight: 0)

let layout = StickyLayout(stickyConfig: stickyConfig)
```

Create an instance of `StickyLayout` with your `StickyConfig` as a parameter, and add it to your `UICollectionView`.
```swift
UICollectionView(frame: .zero, collectionViewLayout: layout)
```

## Installation
StickyLayout is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "StickyLayout"
```

## Feedback and Suggestions
If you have any suggestions or improvements please open a pull request or create an issue.

And if you found StickyLayout useful or want to show support feel free to star this repo!
