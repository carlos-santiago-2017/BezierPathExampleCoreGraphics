# BezierPathExampleCoreGraphics
BezierPathExampleCoreGraphics

``` swift
//
//  SquareView.swift
//  SimpleLines
//
//  Created by Carlos Santiago Cruz on 13/10/18.
//  Copyright © 2018 Carlos Santiago Cruz. All rights reserved.
//

import UIKit

class SquareView: UIView {
    override func draw(_ rect: CGRect) {
       let aPath = UIBezierPath()
        
        // establish line width
        aPath.lineWidth = 8
        
        // establish origin of the line
        aPath.move(to: CGPoint(x:0,y:0))
        
        // establish the end of the line
        aPath.addLine(to: CGPoint(x:frame.width-10,y:0))
        
        // establish the curve
        // This method appends a quadratic Bézier curve from the current point to the end point specified by the endPoint parameter.
        aPath.addQuadCurve(to: CGPoint(x: frame.width, y:10), controlPoint: CGPoint(x:frame.width,y:0))
        
        UIColor.black.set()
        
        aPath.stroke()
    }
}
```
