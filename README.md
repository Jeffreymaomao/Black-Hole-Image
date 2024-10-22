# Black-Hole-Image

This repository is to put the simlation image/result of Kerr / Schwarzschild Black Hole, using the `WebGL` or `Metal`.

## Example file

- `Kerr-4536x2835-1000fs/frame_0.tiff`

    <img src="Kerr-4536x2835-1000fs/frame_0.tiff">

- `Kerr-4536x2835-1000fs/a.mp4`

    <video src="video/kerr-4536x2835-1000fs.mp4">
    </video>

## Note of ffmpeg

- `frame_n.tiff` $\to$ `a.mp4`

    ```bash
    $ ffmpeg -framerate 100 -i frame_%d.tiff -c:v libx264 -crf 18 -preset slow -tune stillimage -pix_fmt yuv420p output.mp4
    ```

    ```bash
    $ ffmpeg -framerate 100 -i frame_%d.tiff -vf "scale=4536:2836" -c:v libx264 -crf 18 -preset slow -pix_fmt yuv420p output.mp4
    ```

    

