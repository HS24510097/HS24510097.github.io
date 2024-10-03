<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Slideshow</title>
    <style>
        * {
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
        }

        .slideshow-container {
            max-width: 1325px;
            position: relative;
            margin: auto;
        }

        .slides {
            display: none;
        }

        img {
            width: 100%;
            height: auto;
        }

        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            width: auto;
            margin-top: -22px;
            padding: 16px;
            color: white;
            font-weight: bold;
            font-size: 18px;
            transition: 0.6s ease;
            border-radius: 0 3px 3px 0;
            user-select: none;
        }

        .next {
            right: 0;
            border-radius: 3px 0 0 3px;
        }

        .prev {
            left: 0;
            border-radius: 3px 0 0 3px;
        }

        .prev:hover, .next:hover {
            background-color: rgba(0,0,0,0.8);
        }

        .resume-container {
            margin-top: 50px;
        }

        .btn {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
        }

        .btn:hover {
            background-color: #45a049;
        }

    </style>
</head>
<body>

    <div class="slideshow-container">
        <div class="slides">
            <img src="Slide1.JPG" alt="Slide 1">
        </div>
        <div class="slides">
            <img src="Slide2.JPG" alt="Slide 2">
        </div>
        <div class="slides">
            <img src="Slide3.JPG" alt="Slide 3">
        </div>
        <div class="slides">
            <img src="Slide4.JPG" alt="Slide 4">
        </div>
        <div class="slides">
            <img src="Slide5.JPG" alt="Slide 5">
        </div>
        <div class="slides">
            <img src="Slide6.JPG" alt="Slide 6">
        </div>
        <div class="slides">
            <img src="Slide7.JPG" alt="Slide 7">
        </div>
        <div class="slides">
            <img src="Slide8.JPG" alt="Slide 8">
        </div>
        <div class="slides">
            <img src="Slide9.JPG" alt="Slide 9">
        </div>
        <div class="slides">
            <img src="Slide10.JPG" alt="Slide 10">
        </div>
        <div class="slides">
            <img src="Slide11.JPG" alt="Slide 11">
        </div>

        <!-- Next and previous buttons -->
        <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
        <a class="next" onclick="plusSlides(1)">&#10095;</a>
    </div>

    <section id="resume" class="resume-container">
        <div class="container">
            <h2>Resume</h2>
            <p>You can view and download my resume below:</p>
            <a href="HS24510097_Lakna Janavie Manimel Wadu.pdf" download="HS24510097_Lakna Janavie Manimel Wadu.pdf" class="btn">Download Resume</a>
        </div>
    </section>

    <script>
        let slideIndex = 0;
        showSlides();

        function showSlides() {
            let i;
            let slides = document.getElementsByClassName("slides");
            for (i = 0; i < slides.length; i++) {
                slides[i].style.display = "none";
            }
            slideIndex++;
            if (slideIndex > slides.length) {slideIndex = 1}
            slides[slideIndex-1].style.display = "block";
            setTimeout(showSlides, 3000);
