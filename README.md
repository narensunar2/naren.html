<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Naren Sunar - Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link rel="icon" type="image" href="https://files.cdn-files-a.com/uploads/5329925/800_679b07189a10b.png?width=600">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: #1a1a1a;
        }

        .profile-card {
            background: #2d2d2d;
            border-radius: 15px;
            padding: 30px;
            width: 320px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            transform: scale(0.95);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            display: grid;
            place-items: center;
        }

        .profile-card:hover {
            transform: scale(1);
            box-shadow: 0 15px 40px rgba(0,0,0,0.4);
        }

        .profile-image {
            width: 150px;
            height: 150px;
           border-radius: 50%;
            margin: 0 auto 20px;
            background-color: white;
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .profile-card:hover .profile-image {
            transform: scale(1.1);
        }

        .profile-name {
             width: 13ch;
            color: #00ff88;
            font-size: 1.8rem;
            margin-bottom: 8px;
            letter-spacing: 1px;
            animation: typing 2s steps(22), blink .5s step-end infinite 
            alternate;
            white-space: nowrap;
            overflow: hidden;
            border-right: 3px solid;
            font-family: monospace;
            font-size: 2em;
        }
        @keyframes typing {
        from {
         width: 0
         }
        }
    
        @keyframes blink {
        50% {
        border-color: transparent
        }
        }

        .profile-title {
            color: #888;
            font-size: 1.1rem;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        .profile-bio {
            color: #aaa;
            line-height: 1.6;
            margin-bottom: 25px;
            font-size: 0.95rem;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .social-link {
            color: #fff;
            font-size: 2rem;
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .social-link:hover {
            transform: translateY(-4px);
        }

        .fa-facebook:hover {
            color: #1877f2;
        }

        .fa-instagram:hover {
            color: #e4405f;
        }

        /* Glowing border effect */
        .profile-card::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #00ff88, transparent);
            z-index: -1;
            border-radius: 17px;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .profile-card:hover::before {
            opacity: 0.19;
        }

        
    </style>
</head>
<body>
    <div class="profile-card">
        <div class="profile-image">
        <img src="https://files.cdn-files-a.com/uploads/5329925/400_679a7d2845fe0.png?width=200" alt="">
        </div>
        <h1 class="profile-name" >Naren Sunar</h1>
        <h2 class="profile-title">Web Designer</h2>
        <p class="profile-bio">
             I'm  in the process of learning. 
        </p>
        <div class="social-links">
            <a href="https://www.facebook.com/narensunar2/" class="social-link">
                <i class="fab fa-facebook"></i>
            </a>
            <a href="https://www.instagram.com/narensunar1/" class="social-link">
                <i class="fab fa-instagram"></i>
            </a>
        </div>
        
    </div>
    <script>
        // Add subtle hover effect to entire card
        const card = document.querySelector('.profile-card');
        
        card.addEventListener('mousemove', (e) => {
            const x = e.clientX - card.getBoundingClientRect().left;
            const y = e.clientY - card.getBoundingClientRect().top;
            
            card.style.transform = `
                scale(1)
                rotateX(${(y - 150) / 25}deg)
                rotateY(${(x - 160) / -25}deg)
            `;
        });

        
        
        
    </script>
</body>
</html>
