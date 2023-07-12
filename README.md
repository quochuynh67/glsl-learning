# glsl-learning

****Một FragmentShader sẽ bao gồm****
 - `gl_FragCoord`: Biến đầu vào để xác định vị trí pixel hiện tại đang cần tính toán.
 - `gl_FragColor`: Biến đầu ra của 1 shader để xác định màu của pixel hiện tại
 - Mọi giá trị `color/coord` nên được chuẩn hoá về `0.0 đến 1.0`



****Ví dụ****

[1. Hệ trục toạ độ tại left-bottom của canvas](left-bottom-coord.md)

<img width="300" alt="image" src="https://github.com/quochuynh67/glsl-learning/assets/38383168/33335a49-18b9-4d70-abfc-cf4e8783cfe0">

------------------------------------------------------------------------------------------------

[2. Di chuyển trục toạ độ về giữa của canvas](center-of-coord.md)

<img width="300" alt="image" src="https://github.com/quochuynh67/glsl-learning/assets/38383168/8da7ca15-e3b3-4a4a-967e-85ec204f474c">
