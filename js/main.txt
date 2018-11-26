
// Get the modal
var modal = document.getElementById('logo_modal');

// Get the image and insert it inside the modal - use its "alt" text as a caption
var imgs = document.querySelectorAll('.img_click');
var modalImg = document.getElementById('img01');
var captionText = document.getElementById('caption');

// Looping for the images adding the click function to display in the modal.
imgs.forEach(images => {
    images.onclick = function(){
        modal.style.display = 'block';
        modalImg.src = this.src;
        captionText.innerHTML = this.alt;
    };
});

// Get the <span> element that closes the modal
var span = document.getElementsByClassName('close')[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() { 
    modal.style.display = 'none';
};

