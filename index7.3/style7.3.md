
/* Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f1f5f9;
    color: #1e293b;
}

/* Header */
.header {
    background-color: #1e293b;
    color: white;
    text-align: center;
    padding: 30px 15px;
}

.header h1 {
    font-size: 32px;
    margin-bottom: 8px;
    color: #38bdf8;
}

.header p {
    color: #cbd5e1;
}

/* Main Container */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 40px 20px;
}

.section-title {
    text-align: center;
    font-size: 30px;
    margin-bottom: 30px;
}

/* Flexbox Product Container */
.product-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: stretch;
    gap: 25px;
}

/* Product Cards */
.product-card {
    background-color: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);

    /* flex-grow | flex-shrink | flex-basis */
    flex: 1 1 240px;

    max-width: 350px;
    display: flex;
    flex-direction: column;

    transition: transform 0.3s, box-shadow 0.3s;
}

.product-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

/* Product Images */
.product-card img {
    width: 100%;
    height: 220px;
    object-fit: cover;
    display: block;
}

/* Product Information */
.product-info {
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    flex-grow: 1;
}

.product-info h3 {
    font-size: 19px;
    margin-bottom: 12px;
}

.price {
    color: #16a34a;
    font-size: 22px;
    font-weight: bold;
    margin-bottom: 18px;
}

/* Button */
.product-info button {
    width: 100%;
    margin-top: auto;
    padding: 12px;
    border: none;
    border-radius: 7px;
    background-color: #2563eb;
    color: white;
    font-size: 15px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.product-info button:hover {
    background-color: #1d4ed8;
}

/* Footer */
.footer {
    text-align: center;
    background-color: #1e293b;
    color: white;
    padding: 20px;
}

/* Tablet */
@media (max-width: 768px) {
    .container {
        padding: 30px 15px;
    }

    .product-container {
        gap: 18px;
    }

    .product-card {
        flex-basis: 200px;
    }

    .product-card img {
        height: 190px;
    }
}

/* Mobile */
@media (max-width: 480px) {
    .header h1 {
        font-size: 27px;
    }

    .section-title {
        font-size: 25px;
    }

    .product-container {
        flex-direction: column;
        align-items: center;
    }

    .product-card {
        flex: 1 1 auto;
        width: 100%;
        max-width: 350px;
    }

    .product-card img {
        height: 220px;
    }
}
