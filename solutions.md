HTML
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profile Card & Product Card Component</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <main class="card-container">
        <!-- 1. Profile Card -->
        <div class="profile-card">
            <span class="card-badge badge-status">Available</span>
            <div class="profile-avatar-wrapper">
                <img src="images/profile.jpg" alt="Atim Akhtar" class="profile-avatar">
            </div>
            <h2 class="profile-name">Atim Akhtar</h2>
            <p class="profile-role">Web Developer & Engineering Student</p>
            <p class="profile-bio">First-year B.Tech CSE student passionate about web development, building clean interfaces, and modern UI components.</p>
            <div class="profile-skills">
                <span class="skill-tag">HTML5</span>
                <span class="skill-tag">CSS3</span>
                <span class="skill-tag">JavaScript</span>
                <span class="skill-tag">Java</span>
            </div>
            <button class="card-button btn-primary">Contact Me</button>
        </div>

        <!-- 2. Product Card -->
        <div class="product-card">
            <span class="card-badge badge-sale">Sale</span>
            <div class="product-image-wrapper">
                <img src="images/project1.jpg" alt="Developer Course Bundle" class="product-image">
            </div>
            <div class="product-info">
                <h2 class="product-title">Full-Stack Web Dev Bundle</h2>
                <div class="product-price-tag">
                    <span class="current-price">₹1,499</span>
                    <span class="original-price">₹2,999</span>
                </div>
                <p class="product-description">Complete course pack covering modern HTML5, CSS3, layout fundamentals, and responsive web design projects.</p>
                <button class="card-button btn-success">Buy Now</button>
            </div>
        </div>
    </main>
</body>
</html>
CSS
/* style.css */

/* Box Model & CSS Reset Setup */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f1f5f9;
    color: #334155;
    line-height: 1.5;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
}

.card-container {
    display: flex;
    gap: 30px;
    flex-wrap: wrap;
    justify-content: center;
    max-width: 900px;
    width: 100%;
}

/* Common Badge Positioning Setup */
.profile-card,
.product-card {
    position: relative;
    background-color: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
    width: 100%;
    max-width: 380px;
    overflow: hidden;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.profile-card:hover,
.product-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

.card-badge {
    position: absolute;
    top: 16px;
    right: 16px;
    padding: 4px 10px;
    font-size: 0.75rem;
    font-weight: bold;
    text-transform: uppercase;
    border-radius: 20px;
    z-index: 10;
}

.badge-status {
    background-color: #dcfce7;
    color: #15803d;
    border: 1px solid #bbf7d0;
}

.badge-sale {
    background-color: #fee2e2;
    color: #b91c1c;
    border: 1px solid #fecaca;
}

/* 1. Profile Card Styling */
.profile-card {
    padding: 32px 24px;
    text-align: center;
}

.profile-avatar-wrapper {
    margin: 0 auto 16px auto;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    border: 3px solid #0284c7;
    padding: 3px;
    background-color: #ffffff;
}

.profile-avatar {
    width: 100%;
    height: 100%;
    border-radius: 50%;
    object-fit: cover;
}

.profile-name {
    font-size: 1.35rem;
    color: #0f172a;
    margin-bottom: 4px;
}

.profile-role {
    font-size: 0.875rem;
    color: #0284c7;
    font-weight: bold;
    margin-bottom: 12px;
}

.profile-bio {
    font-size: 0.9rem;
    color: #64748b;
    margin-bottom: 20px;
}

.profile-skills {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    justify-content: center;
    margin-bottom: 24px;
}

.skill-tag {
    background-color: #f1f5f9;
    color: #475569;
    font-size: 0.75rem;
    font-weight: bold;
    padding: 4px 10px;
    border-radius: 6px;
    border: 1px solid #e2e8f0;
}

/* 2. Product Card Styling */
.product-image-wrapper {
    width: 100%;
    height: 180px;
    background-color: #f8fafc;
}

.product-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.product-info {
    padding: 24px;
}

.product-title {
    font-size: 1.25rem;
    color: #0f172a;
    margin-bottom: 8px;
}

.product-price-tag {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 12px;
}

.current-price {
    font-size: 1.35rem;
    font-weight: bold;
    color: #0f172a;
}

.original-price {
    font-size: 0.9rem;
    color: #94a3b8;
    text-decoration: line-through;
}

.product-description {
    font-size: 0.9rem;
    color: #64748b;
    margin-bottom: 20px;
}

/* General Button Styles */
.card-button {
    width: 100%;
    padding: 10px 16px;
    font-size: 0.95rem;
    font-weight: bold;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: background-color 0.2s ease;
}

.btn-primary {
    background-color: #0284c7;
    color: #ffffff;
}

.btn-primary:hover {
    background-color: #0369a1;
}

.btn-success {
    background-color: #16a34a;
    color: #ffffff;
}

.btn-success:hover {
    background-color: #15803d;
}