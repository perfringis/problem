# Problem

## Question

How do I get the closest possible image to the original using vector graphics?

## Description of the problem

I have a collection of 105 vector graphics. The graphics are available in a folder named "vector graphics". For the purpose of presenting the problem, you can assume that it is a collection of symbols or icons.

### What operations can be performed on a single graphic/layer?

- Move(from place to another),
- Scaling(zooming in or out the graphic without deforming it),
- Transformation(i.e., modifying the graphic by length or width),
- Rotation(i.e., rotation a few(or more) degrees),
- Flipping(i.e., horizontally or vertically),

From the main set of 105 vector graphics, we can select only 40 graphics. In a subset of 40
graphics, one graphic may appear several times.

Based on the 40 graphics from this point, a reconstruction is performed on the original
image.

### Scene

Graphics are placed on a 966px by 966px scene. Graphics are visible only in the scene area. If part of the graphic slightly is beyond the edge of the scene, only the part that is within the scene area is visible.

### Layer system

One graphic is equivalent to one layer. This means that we have 40 layers. The layer system
We can think of as a plate with a stack of pancakes stacked on top of each other. 
Layer #1 is the topmost layer. The graphic on this layer is seen first by the observer. Layer #2 is seen second by the observer. This means that the graphic from layer #1 can cover completely or slightly(or not cover at all) the graphic from layer #2. This mechanism is applied to all 40 layers. This system of layers is known from programs like "Photoshop" and others used for processing vector or raster graphics.

### Colors

Coloring and sampling in my opinion is the simplest process. The open-cv library has a large
range of algorithms.

### Additional comments

It would be nice if the program could "experiment" with graphics in a "smart" way. It means that the program can replace all 40 graphics or some of them or none of them during the learning phase. It means, that it could determine the most optimal set of 40 graphics that could reconstruct as close as possible the original image.

The second important aspect related to comment no. 1. It would be nice if the program could "experiment" and was able to "shuffle" 40 layers and was able to generate the most optimal order of layers.