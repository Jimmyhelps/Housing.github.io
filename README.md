<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Paperworks - Student Accommodation Sheffield</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background: linear-gradient(to right, #1a2a6c, #b21f1f, #fdbb2d);
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .tagline {
            font-size: 1.2rem;
            margin-bottom: 20px;
        }
        
        .alert-banner {
            background-color: #ffc107;
            color: #333;
            padding: 10px;
            text-align: center;
            font-weight: bold;
        }
        
        .nav {
            background-color: #343a40;
            padding: 15px 0;
        }
        
        .nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
        }
        
        .nav li {
            margin: 0 15px;
        }
        
        .nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav a:hover {
            color: #fdbb2d;
        }
        
        .hero {
            background: url('https://images.unsplash.com/photo-1560448204-e02f11c3d0e2?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80') no-repeat center center/cover;
            height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
            position: relative;
        }
        
        .hero::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
        }
        
        .hero-content {
            z-index: 1;
            max-width: 800px;
            padding: 20px;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background: #fdbb2d;
            color: #333;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background 0.3s;
        }
        
        .btn:hover {
            background: #ffa000;
        }
        
        .section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: #1a2a6c;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .feature-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-img {
            height: 200px;
            overflow: hidden;
        }
        
        .feature-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .feature-card:hover .feature-img img {
            transform: scale(1.1);
        }
        
        .feature-content {
            padding: 20px;
        }
        
        .feature-content h3 {
            color: #1a2a6c;
            margin-bottom: 10px;
        }
        
        .map-container {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 40px;
        }
        
        .map {
            height: 400px;
            background: #eee;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .studios {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .studio-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .studio-img {
            height: 200px;
            overflow: hidden;
        }
        
        .studio-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .studio-content {
            padding: 20px;
        }
        
        .studio-content h3 {
            color: #1a2a6c;
            margin-bottom: 10px;
        }
        
        .price {
            color: #b21f1f;
            font-weight: bold;
            font-size: 1.2rem;
            margin: 10px 0;
        }
        
        .contact-info {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 40px;
            text-align: center;
        }
        
        .contact-methods {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 30px;
        }
        
        .contact-method {
            flex: 1;
            min-width: 250px;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 8px;
            text-align: center;
        }
        
        .contact-method i {
            font-size: 2rem;
            color: #1a2a6c;
            margin-bottom: 15px;
        }
        
        footer {
            background: #343a40;
            color: white;
            text-align: center;
            padding: 30px 0;
            margin-top: 60px;
        }
        
        @media (max-width: 768px) {
            .nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            .nav li {
                margin: 5px 0;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">The Paperworks</div>
            <div class="tagline">Premium Student Accommodation in Sheffield</div>
        </div>
    </header>
    
    <div class="alert-banner">
        🎓 Immediate Tenancy Takeover Available - £500 Cashback! 🎓
    </div>
    
    <div class="nav">
        <div class="container">
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#location">Location</a></li>
                <li><a href="#studios">Studios</a></li>
                <li><a href="#amenities">Amenities</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </div>
    
    <div class="hero">
        <div class="hero-content">
            <h1>Student Living Made Perfect</h1>
            <p>Modern, affordable accommodation in the heart of Sheffield. Just minutes from universities, transport, and city center.</p>
            <a href="#contact" class="btn">Inquire Now</a>
        </div>
    </div>
    
    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title">About The Paperworks</h2>
            <div class="features">
                <div class="feature-card">
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1592424002053-21f369ad7fdb?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Building Exterior">
                    </div>
                    <div class="feature-content">
                        <h3>Modern Student Living</h3>
                        <p>The Paperworks offers contemporary student accommodation in the heart of Sheffield. Our Silver Ensuite rooms provide comfortable living with shared kitchen facilities.</p>
                    </div>
                </div>
                
                <div class="feature-card">
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1586023492125-27b2c045efd7?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Room Interior">
                    </div>
                    <div class="feature-content">
                        <h3>Affordable Luxury</h3>
                        <p>At just £95 per week with all bills included, our rooms offer exceptional value. Currently available with £500 cashback on tenancy takeover!</p>
                    </div>
                </div>
                
                <div class="feature-card">
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1555854877-bab0e3786836?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Student Life">
                    </div>
                    <div class="feature-content">
                        <h3>Perfect for Students</h3>
                        <p>Designed with students in mind, The Paperworks offers a vibrant community atmosphere with plenty of study and social spaces.</p>
                    </div>
                </div>
            </div>
            
            <div class="map-container">
                <h3>Prime Location in Sheffield</h3>
                <p>The Paperworks is situated at York Street, Sheffield, S1 2NY, in the perfect location for students:</p>
                <ul>
                    <li>🚊 2 min walk to Tram Stop</li>
                    <li>🏫 6 min walk to Sheffield Hallam University (City Campus)</li>
                    <li>🚌 8 min walk to Sheffield Interchange</li>
                    <li>🛒 2 min walk to Lidl</li>
                    <li>🏙️ 9 min walk to City Centre</li>
                </ul>
                <div class="map">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2379.379066756098!2d-1.465623723005019!3d53.381075472402!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4879786c66cfd38d%3A0xc5f39a5c6939282e!2sYork%20St%2C%20Sheffield%2C%20UK!5e0!3m2!1sen!2sus!4v1689877258967!5m2!1sen!2sus" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>
    
    <section id="studios" class="section">
        <div class="container">
            <h2 class="section-title">Available Studio Apartments</h2>
            <div class="studios">
                <div class="studio-card">
                    <div class="studio-img">
                        <img src="https://images.unsplash.com/photo-1522708323590-d24dbb6b0267?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Studio 1">
                    </div>
                    <div class="studio-content">
                        <h3>Silver Studio</h3>
                        <p>Compact and efficient studio with ensuite bathroom and kitchenette.</p>
                        <div class="price">£95/week</div>
                    </div>
                </div>
                
                <div class="studio-card">
                    <div class="studio-img">
                        <img src="https://images.unsplash.com/photo-1567767292278-a4f21aa2d36e?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Studio 2">
                    </div>
                    <div class="studio-content">
                        <h3>Gold Studio</h3>
                        <p>Spacious studio with premium finishes and additional storage space.</p>
                        <div class="price">£115/week</div>
                    </div>
                </div>
                
                <div class="studio-card">
                    <div class="studio-img">
                        <img src="https://images.unsplash.com/photo-1598228723793-52759bba239c?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Studio 3">
                    </div>
                    <div class="studio-content">
                        <h3>Platinum Studio</h3>
                        <p>Luxury studio with premium amenities and stunning city views.</p>
                        <div class="price">£135/week</div>
                    </div>
                </div>
                
                <div class="studio-card">
                    <div class="studio-img">
                        <img src="https://images.unsplash.com/photo-1574362848149-11496d93a7c7?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Studio 4">
                    </div>
                    <div class="studio-content">
                        <h3>Diamond Studio</h3>
                        <p>Top-tier studio with separate living and sleeping areas.</p>
                        <div class="price">£155/week</div>
                    </div>
                </div>
                
                <div class="studio-card">
                    <div class="studio-img">
                        <img src="https://images.unsplash.com/photo-1583608205776-bfd35f0d9f83?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Studio 5">
                    </div>
                    <div class="studio-content">
                        <h3>Executive Studio</h3>
                        <p>Premium studio with high-end finishes and extra living space.</p>
                        <div class="price">£175/week</div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="amenities" class="section">
        <div class="container">
            <h2 class="section-title">Amenities & Facilities</h2>
            <div class="features">
                <div class="feature-card">
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Gym">
                    </div>
                    <div class="feature-content">
                        <h3>On-site Gym</h3>
                        <p>Stay fit without leaving the building with our fully-equipped gym.</p>
                    </div>
                </div>
                
                <div class="feature-card">
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1542204165-65bf26472b9b?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Cinema">
                    </div>
                    <div class="feature-content">
                        <h3>Cinema/Theatre Room</h3>
                        <p>Enjoy movie nights with friends in our private cinema room.</p>
                    </div>
                </div>
                
                <div class="feature-card">
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1550745165-9bc0b252726f?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Games Room">
                    </div>
                    <div class="feature-content">
                        <h3>Games Room</h3>
                        <p>Unwind with pool, foosball, and video games in our entertainment space.</p>
                    </div>
                </div>
                
                <div class="feature-card">
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1504384308090-c894fdcc538d?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Study Space">
                    </div>
                    <div class="feature-content">
                        <h3>Study Spaces</h3>
                        <p>Quiet areas designed for focused studying and academic success.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="contact" class="section">
        <div class="container">
            <h2 class="section-title">Contact Us</h2>
            <div class="contact-info">
                <p>Interested in the immediate tenancy takeover or want to learn more about our available studios? Reach out to us today!</p>
                
                <div class="contact-methods">
                    <div class="contact-method">
                        <i class="fab fa-whatsapp"></i>
                        <h3>WhatsApp</h3>
                        <p>+44 7367067339</p>
                    </div>
                    
                    <div class="contact-method">
                        <i class="fas fa-envelope"></i>
                        <h3>Email</h3>
                        <p>Shefielduni@proton.me</p>
                    </div>
                    
                    <div class="contact-method">
                        <i class="fas fa-map-marker-alt"></i>
                        <h3>Address</h3>
                        <p>The Paperworks, York Street, Sheffield, S1 2NY</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <p>&copy; 2023 The Paperworks Student Accommodation. All rights reserved.</p>
            <p>Designed for students, by students.</p>
        </div>
    </footer>
</body>
</html>
