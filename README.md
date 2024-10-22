# Black-Hole-Image

This repository is to put the simlation image/result of Kerr / Schwarzschild Black Hole, using the `WebGL` or `Metal`.

## Example

**Click image to see video on YouTube**

<a href="https://youtu.be/bswZj-eAFSk?si=TCcypM0hRnJySV0z"><img src="./kerr-4536x2835-1000fs-frame_0.jpg"></a>

- Download video: [`video/kerr-4536x2835-1000fs.mp4`](https://github.com/Jeffreymaomao/Black-Hole-Image/raw/refs/heads/main/video/kerr-4536x2835-1000fs.mp4)
- Download TIFF image (Kerr Black hole):
    - [`kerr-4536x2835-1000fs/frame_0.tiff`](https://github.com/Jeffreymaomao/Black-Hole-Image/raw/refs/heads/main/Kerr-4536x2835-1000fs/frame_0.tiff)
    - [`kerr-1428x844-100fs/frame_0.tiff`](https://github.com/Jeffreymaomao/Black-Hole-Image/raw/refs/heads/main/kerr-1428x844-100fs/frame_0.tiff)

## Note of ffmpeg

- `frame_n.tiff` $\to$ `a.mp4`

    ```bash
    $ ffmpeg -framerate 100 -i frame_%d.tiff -c:v libx264 -crf 18 -preset slow -tune stillimage -pix_fmt yuv420p output.mp4
    ```

    ```bash
    $ ffmpeg -framerate 100 -i frame_%d.tiff -vf "scale=4536:2836" -c:v libx264 -crf 18 -preset slow -pix_fmt yuv420p output.mp4
    ```

    

