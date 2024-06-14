<script>
    let imageUrl = "https://picsum.photos/200";
    // A string variable containing the URL of the image.

    let caption = "Caption of Image";
    // A string variable containing the caption for the image.

    let linkUrl = "https://picsum.photos/200";
    // A string variable containing the URL to which the image is linked.
</script>

<figure>
    <a href={linkUrl}>
        <!-- An anchor element that wraps the image, making the image a clickable link. -->

        <img src={imageUrl} alt={caption} />
        <!-- An image element that uses imageUrl for the src attribute and caption for the alt attribute. -->
    </a>
    <figcaption>
        <!-- Displays the caption variable as the caption for the image. -->
        {caption}
    </figcaption>
</figure>

<style>
    figure {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1rem;
        padding: 1.5rem;
        width: fit-content;
        border-radius: 10px;
        box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
        /* Adds a shadow around the figure. */

        backdrop-filter: blur(4px);
        /* Applies a blur effect to the background. */

        background: rgba(98, 217, 255, 0.25);
        background-color: blueviolet;
    }
</style>
