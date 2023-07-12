```glsl
void mainImage( out vec4 fragColor, in vec2 fragCoord )
{
vec2 r = vec2( fragCoord.xy / iResolution.xy );
	
	vec3 backgroundColor = vec3(1.0);
	vec3 axesColor = vec3(0.0, 0.0, 1.0);
	vec3 gridColor = vec3(0.5);

	// start by setting the background color. If pixel's value
	// is not overwritten later, this color will be displayed.
	vec3 pixel = backgroundColor;
	
	// Draw the grid lines
	// we used "const" because loop variables can only be manipulated
	// by constant expressions.
	const float tickWidth = 0.1;
    
    // Cách 1: for loop
	//for(float i=0.0; i<1.0; i+=tickWidth) {
	//	// "i" is the line coordinate.
	//	if(abs(r.x - i)<0.002) pixel = gridColor;
	//	if(abs(r.y - i)<0.002) pixel = gridColor;
	//}
    
    
    // Cách 2: mod 
	//if( mod(r.x, tickWidth) < 0.008 ) pixel = gridColor;
    //if( mod(r.y, tickWidth) < 0.008 ) pixel = gridColor;
	
	
    
    //Cách 3: For đối xứng tâm
    for(float i=-2.0; i<2.0; i+=tickWidth) {
		// "i" is the line coordinate.
		if(abs(r.x - i)<0.004) pixel = gridColor;
		if(abs(r.y - i)<0.004) pixel = gridColor;
	}

fragColor = vec4(pixel, 1.0);
}
```
