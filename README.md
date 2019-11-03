## Force field guide

As seen in the workshop shaders can be used to change things about objects. The example showed you how to apply simple color changes, but you will now alter the entire appearance of an object. 

Start off by creating a new PBR shader and applying it as a material to a sphere.

First things first, a force field is for the most part transparent. Open the settings on your master node and make its surface transparent.

A force field effect is a lot like a light reflector that looks different depending on the angle that you look at it. This is called a Fresnel Effect. Create such a node.

Once created, connect it to the Alpha value on your master node. If save now you should see the sphere is transparent, but still has an outline.

To make it a bit more force field like, give your master node a color. As the force field should emit color, you shouldn’t assign it to the Albedo of your master node.

Now, this force field looks a bit dull and possibly a bit strange. First, make it visible from the inside.

To make it look a bit more interesting, you can add some extra effects. 

To add some texture over the force field, you can add a Voronoi Effect. This is a noise type effect. The Voronoi Effect is good for simple effects like this. It is also often used to simulate water. To apply the Voronoi effect, multiply it with the Fresnel Effect.

The last part will be up to you. The Voronoi is not moving. Try to get it to move over the area of the force field. A tip, you will want to change the offset.

As a final exercise, make the following items editable from the Unity inspector.

* The “power” of the force field
* The color of the force field
* The speed of the movement of the Voronoi effect

When you’re done, you can open the unity sample project linked in a mail you received earlier. Choose an effect and recreate it. We recommend the dissolve shader, and try to apply it to one of your own games (for example when an enemy dies).

