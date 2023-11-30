<div class="home-page">
    <div class="home-page-title">
        a winter in japan
    </div>
    <div class="home-page-content">
        <div class="home-page-content-one">
            a small collection of photos to show the variety of life in japan, even in winter
        </div>
    </div>
</div>


<div id="main-page-photo-container"></div>

<script>
    const accessKey = 'toXT5SQcrntQACLJ_zmxrkws1PjG41aLk_c5Fl2AfPM';
    const username = 'ohkay';
    let imgs = [];

    const getLikedPhotos = async () => {
        try {
            const response = await fetch(`https://api.unsplash.com/users/${username}/likes`, {
                headers: {
                    Authorization: `Client-ID ${accessKey}`,
                },
            });

            if (!response.ok) {
                throw new Error(`HTTP error! Status: ${response.status}`);
            }

            const data = await response.json();
            imgs = data;

            
            const photoContainer = document.getElementById('main-page-photo-container');
            imgs.forEach(photo => {
                const img = document.createElement('img');
                img.src = photo.urls.regular;
                img.alt = photo.description || 'photo of japan in winter';
                photoContainer.appendChild(img);
            });

        } catch (error) {
            console.error('Error fetching or displaying liked photos:', error);
        }
    };

    // Call the function to get liked photos
    getLikedPhotos();
</script>


