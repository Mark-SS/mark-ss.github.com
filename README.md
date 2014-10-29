mark-ss.github.com
==================
```swift
override init(frame: CGRect) {
    super.init(frame: frame)
 
    trackLayer.backgroundColor = UIColor.blueColor().CGColor
    layer.addSublayer(trackLayer)
 
    lowerThumbLayer.backgroundColor = UIColor.greenColor().CGColor
    layer.addSublayer(lowerThumbLayer)
 
    upperThumbLayer.backgroundColor = UIColor.greenColor().CGColor
    layer.addSublayer(upperThumbLayer)
 
    updateLayerFrames()
}
 
required init(coder: NSCoder) {
    super.init(coder: coder)
}
 
func updateLayerFrames() {
    trackLayer.frame = bounds.rectByInsetting(dx: 0.0, dy: bounds.height / 3)
    trackLayer.setNeedsDisplay()
 
    let lowerThumbCenter = CGFloat(positionForValue(lowerValue))
 
    lowerThumbLayer.frame = CGRect(x: lowerThumbCenter - thumbWidth / 2.0, y: 0.0,
      width: thumbWidth, height: thumbWidth)
    lowerThumbLayer.setNeedsDisplay()
 
    let upperThumbCenter = CGFloat(positionForValue(upperValue))
    upperThumbLayer.frame = CGRect(x: upperThumbCenter - thumbWidth / 2.0, y: 0.0,
        width: thumbWidth, height: thumbWidth)
    upperThumbLayer.setNeedsDisplay()
}
 
func positionForValue(value: Double) -> Double {
    let widthDouble = Double(thumbWidth)
    return Double(bounds.width - thumbWidth) * (value - minimumValue) /
        (maximumValue - minimumValue) + Double(thumbWidth / 2.0)
}
```
