<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CurlKraft Organics</title>
  <script src="https://cdn.jsdelivr.net/npm/react@18.2.0/umd/react.development.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/react-dom@18.2.0/umd/react-dom.development.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@babel/standalone@7.20.15/babel.min.js"></script>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Lato:wght@400&display=swap" rel="stylesheet">
  <style>
    body {
      background-image: url('https://www.transparenttextures.com/patterns/kraft-paper.png');
      background-color: #F5F5F5; /* Coconut White */
    }
    .playfair {
      font-family: 'Playfair Display', serif;
    }
    .lato {
      font-family: 'Lato', sans-serif;
    }
  </style>
</head>
<body>
  <div id="root"></div>
  <script type="text/babel">
    function Header() {
      return (
        <header className="bg-[#1A3C34] text-[#F5F5F5] sticky top-0 z-10">
          <nav className="container mx-auto flex justify-between items-center py-4">
            <h1 className="text-3xl playfair font-bold text-[#D4A017]">CurlKraft Organics</h1>
            <ul className="flex space-x-6 lato text-sm">
              <li><a href="#home" className="hover:text-[#E84A6E]">Home</a></li>
              <li><a href="#products" className="hover:text-[#E84A6E]">Products</a></li>
              <li><a href="#about" className="hover:text-[#E84A6E]">About</a></li>
              <li><a href="#contact" className="hover:text-[#E84A6E]">Contact</a></li>
            </ul>
          </nav>
        </header>
      );
    }

  function Hero() {
      return (
        <section id="home" className="bg-[#F5F5F5] py-20 relative">
          <div className="container mx-auto text-center">
            <h2 className="text-5xl playfair font-bold text-[#1A3C34] mb-4">Embrace Your Natural Curls</h2>
            <p className="text-lg lato text-[#8B5A2B] mb-6 max-w-2xl mx-auto">Discover CurlKraft Organics – premium, eco-friendly hair care crafted for curly hair with organic pitaya and manuka honey.</p>
            <a href="#products" className="bg-[#E84A6E] text-[#F5F5F5] px-6 py-3 rounded-full hover:bg-[#F28C38] lato">Shop Now</a>
          </div>
          <div className="absolute inset-0 opacity-10 pointer-events-none" style={{ background: 'url(https://www.transparenttextures.com/patterns/honeycomb.png)' }}></div>
        </section>
      );
    }

  function ProductCard({ name, description, price }) {
      return (
        <div className="bg-[#F5F5F5] p-6 rounded-lg shadow-md relative">
          <div className="h-48 bg-[#1A3C34] mb-4 rounded flex items-center justify-center">
            <img src="https://via.placeholder.com/100?text=Pitaya" alt="Pitaya" className="w-24 h-24 rounded-full border-2 border-[#D4A017]" />
          </div>
          <h3 className="text-xl playfair font-semibold text-[#E84A6E]">{name}</h3>
          <p className="text-[#8B5A2B] lato mt-2 text-sm">Ecocert-Certified, 82.82% Organic</p>
          <p className="text-[#F5F5F5] lato mt-1 text-xs bg-[#1A3C34] p-2 rounded">{description}</p>
          <p className="text-[#F28C38] lato font-bold mt-4">${price}</p>
          <button className="mt-4 bg-[#F28C38] text-[#F5F5F5] px-4 py-2 rounded hover:bg-[#E84A6E] lato">Add to Cart</button>
          <div className="flex justify-center gap-2 mt-4">
            <span className="bg-[#F28C38] text-[#F5F5F5] text-xs lato px-2 py-1 rounded">Ecocert</span>
            <span className="bg-[#F28C38] text-[#F5F5F5] text-xs lato px-2 py-1 rounded">100% Natural</span>
            <span className="bg-[#D4A017] text-[#1A3C34] text-xs lato px-2 py-1 rounded">Made in Brussels</span>
          </div>
          <div className="absolute inset-0 opacity-20 pointer-events-none" style={{ background: 'url(https://www.transparenttextures.com/patterns/green-leaves.png)' }}></div>
        </div>
      );
    }

  function Products() {
      const products = [
        { name: "Organic Pitaya & Manuka Honey Shampoo", description: "Gently cleanses and hydrates curls with a tropical glow.", price: 14.99 },
        { name: "Organic Pitaya & Manuka Honey Conditioner", description: "Detangles and moisturizes curls with a silky finish.", price: 16.99 },
        { name: "Organic Pitaya & Manuka Honey Leave-In Mask/Curling Cream 2-in-1", description: "Nourishes, defines curls, and fights frizz with dual-action care.", price: 19.99 },
        { name: "Organic Pitaya & Manuka Honey Serum Treatment", description: "Repairs and adds shine with lightweight, non-greasy hydration.", price: 22.99 },
      ];

     return (
        <section id="products" className="py-16 bg-[#F5F5F5]">
          <div className="container mx-auto">
            <h2 className="text-4xl playfair font-bold text-center text-[#1A3C34] mb-8">Our Products</h2>
            <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
              {products.map((product, index) => (
                <ProductCard key={index} {...product} />
              ))}
            </div>
          </div>
        </section>
      );
    }

    function About() {
      return (
        <section id="about" className="py-16 bg-[#F5F5F5]">
          <div className="container mx-auto text-center">
            <h2 className="text-4xl playfair font-bold text-[#1A3C34] mb-6">About CurlKraft Organics</h2>
            <p className="text-[#8B5A2B] lato max-w-2xl mx-auto text-lg">
              At CurlKraft Organics, we celebrate natural beauty with sustainable, organic ingredients like pitaya, manuka honey, and neroli. Our products are handcrafted in Brussels to nourish curly hair while being kind to the planet.
            </p>
          </div>
        </section>
      );
    }

    function Contact() {
      return (
        <section id="contact" className="py-16 bg-[#F5F5F5]">
          <div className="container mx-auto text-center">
            <h2 className="text-4xl playfair font-bold text-[#1A3C34] mb-6">Get in Touch</h2>
            <p className="text-[#8B5A2B] lato mb-4 text-lg">Have questions? Reach out to us!</p>
            <p className="text-[#8B5A2B] lato">Email: support@curlkraftorganics.com</p>
            <p className="text-[#8B5A2B] lato">Phone: (555) 123-4567</p>
          </div>
        </section>
      );
    }

    function Footer() {
      return (
        <footer className="bg-[#1A3C34] text-[#F5F5F5] py-6">
          <div className="container mx-auto text-center">
            <p className="lato">© 2025 CurlKraft Organics. All rights reserved.</p>
            <div className="mt-4 flex justify-center space-x-6 lato">
              <a href="https://www.etsy.com/shop/CurlKraftOrganics" target="_blank" rel="noopener noreferrer" className="hover:text-[#E84A6E]">Shop on Etsy</a>
              <a href="https://www.instagram.com/curlkraftorganics" target="_blank" rel="noopener noreferrer" className="hover:text-[#E84A6E]">Follow on Instagram</a>
            </div>
          </div>
        </footer>
      );
    }

    function App() {
      return (
        <div>
          <Header />
          <Hero />
          <Products />
          <About />
          <Contact />
          <Footer />
        </div>
      );
    }

    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(<App />);
  </script>
</body>
</html>
