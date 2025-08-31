tipsschool-website/
 ├─ public/
 │   ├─ index.html
 │   └─ assets/
 │       ├─ logo.png
 │       ├─ hero.jpg
 │       ├─ gallery1.jpg
 │       ├─ gallery2.jpg
 │       └─ gallery3.jpg
 ├─ src/
 │   ├─ components/
 │   │   ├─ Navbar.jsx
 │   │   ├─ Footer.jsx
 │   │   └─ Card.jsx
 │   ├─ pages/
 │   │   ├─ Home.jsx
 │   │   ├─ About.jsx
 │   │   ├─ Admissions.jsx
 │   │   ├─ Academics.jsx
 │   │   ├─ News.jsx
 │   │   ├─ Events.jsx
 │   │   ├─ Gallery.jsx
 │   │   └─ Contact.jsx
 │   ├─ i18n.js
 │   ├─ App.jsx
 │   └─ main.jsx
 ├─ index.css
 ├─ tailwind.config.js
 └─ package.json
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>TIPS SCHOOL</title>
</head>
<body>
  <div id="root"></div>
</body>
</html>
{
  "name": "tipsschool-website",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "framer-motion": "^10.12.16",
    "i18next": "^23.4.7",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-i18next": "^13.2.2",
    "react-router-dom": "^6.16.0"
  },
  "devDependencies": {
    "autoprefixer": "^11.10.0",
    "postcss": "^8.4.32",
    "tailwindcss": "^3.3.3",
    "vite": "^5.1.0"
  }
}
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html", "./src/**/*.{js,jsx}"],
  theme: { extend: {} },
  plugins: [],
};
@tailwind base;
@tailwind components;
@tailwind utilities;

body {
  font-family: 'Arial', sans-serif;
}
import i18n from 'i18next';
import { initReactI18next } from 'react-i18next';

const resources = {
  en: {
    translation: {
      welcome: "Welcome to TIPS SCHOOL",
      about: "About Us",
      admissions: "Admissions",
      academics: "Academics",
      news: "News",
      events: "Events",
      gallery: "Gallery",
      contact: "Contact Us"
    }
  },
  ur: {
    translation: {
      welcome: "ٹی آئی پی ایس اسکول میں خوش آمدید",
      about: "ہمارے بارے میں",
      admissions: "داخلہ",
      academics: "نصاب",
      news: "خبریں",
      events: "تقریبات",
      gallery: "گیلری",
      contact: "ہم سے رابطہ کریں"
    }
  }
};

i18n.use(initReactI18next).init({
  resources,
  lng: "en",
  fallbackLng: "en",
  interpolation: { escapeValue: false }
});

export default i18n;
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
import "./index.css";
import "./i18n";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
import React from "react";
import { BrowserRouter as Router, Routes, Route } from "react-router-dom";
import Navbar from "./components/Navbar";
import Footer from "./components/Footer";
import Home from "./pages/Home";
import About from "./pages/About";
import Admissions from "./pages/Admissions";
import Academics from "./pages/Academics";
import News from "./pages/News";
import Events from "./pages/Events";
import Gallery from "./pages/Gallery";
import Contact from "./pages/Contact";

const App = () => (
  <Router>
    <Navbar />
    <Routes>
      <Route path="/" element={<Home />} />
      <Route path="/about" element={<About />} />
      <Route path="/admissions" element={<Admissions />} />
      <Route path="/academics" element={<Academics />} />
      <Route path="/news" element={<News />} />
      <Route path="/events" element={<Events />} />
      <Route path="/gallery" element={<Gallery />} />
      <Route path="/contact" element={<Contact />} />
    </Routes>
    <Footer />
  </Router>
);

export default App;
import React from 'react';
import { Link } from 'react-router-dom';
import { useTranslation } from 'react-i18next';
import logo from '../assets/logo.png';

const Navbar = () => {
  const { t, i18n } = useTranslation();
  return (
    <nav className="bg-blue-900 text-white p-4 sticky top-0 z-50">
      <div className="flex justify-between items-center container mx-auto">
        <div className="flex items-center space-x-2">
          <img src={logo} alt="TIPS SCHOOL" className="h-10 w-10"/>
          <span className="font-bold text-xl">TIPS SCHOOL</span>
        </div>
        <ul className="flex space-x-4">
          <li><Link to="/">{t('welcome')}</Link></li>
          <li><Link to="/about">{t('about')}</Link></li>
          <li><Link to="/admissions">{t('admissions')}</Link></li>
          <li><Link to="/academics">{t('academics')}</Link></li>
          <li><Link to="/news">{t('news')}</Link></li>
          <li><Link to="/events">{t('events')}</Link></li>
          <li><Link to="/gallery">{t('gallery')}</Link></li>
          <li><Link to="/contact">{t('contact')}</Link></li>
        </ul>
        <div className="space-x-2">
          <button onClick={() => i18n.changeLanguage('en')} className="px-2 py-1 border rounded">EN</button>
          <button onClick={() => i18n.changeLanguage('ur')} className="px-2 py-1 border rounded">UR</button>
        </div>
      </div>
    </nav>
  );
};

export default Navbar;
import React from "react";

const Footer = () => (
  <footer className="bg-blue-900 text-white py-6 mt-10 text-center">
    <p>© 2025 TIPS SCHOOL. All rights reserved.</p>
    <div className="flex justify-center space-x-4 mt-2">
      <a href="#" className="hover:text-yellow-400">Facebook</a>
      <a href="#" className="hover:text-yellow-400">Twitter</a>
      <a href="#" className="hover:text-yellow-400">Instagram</a>
    </div>
  </footer>
);

export default Footer;
import React from "react";

const Card = ({ title, description, image }) => (
  <div className="border rounded shadow-lg p-4 hover:shadow-xl transition">
    {image && <img src={image} alt={title} className="w-full h-40 object-cover rounded mb-4"/>}
    <h3 className="font-bold text-xl mb-2">{title}</h3>
    <p>{description}</p>
  </div>
);

export default Card;
import React from "react";
import { useTranslation } from "react-i18next";
import Card from "../components/Card";
import hero from "../assets/hero.jpg";
import gallery1 from "../assets/gallery1.jpg";

const Home = () => {
  const { t } = useTranslation();
  return (
    <div className="container mx-auto p-8">
      <div className="mb-8">
        <img src={hero} alt="Hero" className="w-full h-64 object-cover rounded"/>
        <h1 className="text-4xl font-bold mt-4">{t('welcome')}</h1>
      </div>
      <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
        <Card title="Student Success" description="Our students excel in academics." image={gallery1} />
        <Card title="Extra Activities" description="Sports, arts, and clubs." image={gallery1} />
        <Card title="Achievements" description="Awards and recognitions." image={gallery1} />
      </div>
    </div>
  );
};

export default Home;
import React from "react";
import { useTranslation } from "react-i18next";

const About = () => {
  const { t } = useTranslation();
  return (
    <div className="container mx-auto p-8">
      <h1 className="text-4xl font-bold mb-6">{t('about')}</h1>
      <p className="mb-4">
        TIPS SCHOOL was founded with the mission to provide quality education and
        holistic development for students. Our vision is to create future leaders
        with knowledge, ethics, and skills.
      </p>
      <h2 className="text-2xl font-semibold mt-6 mb-2">Our Mission & Vision</h2>
      <p className="mb-4">
        Our mission is to foster academic excellence, creativity, and social responsibility.
        We aim to nurture well-rounded individuals prepared for the challenges of tomorrow.
      </p>
      <h2 className="text-2xl font-semibold mt-6 mb-2">Principal's Message</h2>
      <p>
        Welcome to TIPS SCHOOL! We believe in empowering students through
        innovative teaching, modern facilities, and a caring environment.
      </p>
    </div>
  );
};

export default About;
import React from "react";
import { useTranslation } from "react-i18next";

const Admissions = () => {
  const { t } = useTranslation();
  return (
    <div className="container mx-auto p-8">
      <h1 className="text-4xl font-bold mb-6">{t('admissions')}</h1>
      <p className="mb-4">
        Welcome to the admissions section. Join TIPS SCHOOL and be part of our thriving academic community.
      </p>
      <h2 className="text-2xl font-semibold mt-6 mb-2">Admission Process</h2>
      <ol className="list-decimal list-inside mb-4">
        <li>Submit online application</li>
        <li>Schedule assessment/interview</li>
        <li>Receive admission decision</li>
        <li>Complete enrollment formalities</li>
      </ol>
      <h2 className="text-2xl font-semibold mt-6 mb-2">Fees & Scholarships</h2>
      <p>
        Our fee structure is transparent and competitive. Scholarships are available
        for deserving students based on merit and need.
      </p>
    </div>
  );
};

export default Admissions;
import React from "react";
import Card from "../components/Card";
import { useTranslation } from "react-i18next";
import gallery2 from "../assets/gallery2.jpg";

const Academics = () => {
  const { t } = useTranslation();
  return (
    <div className="container mx-auto p-8">
      <h1 className="text-4xl font-bold mb-6">{t('academics')}</h1>
      <p className="mb-6">
        At TIPS SCHOOL, we offer a comprehensive curriculum with focus on both academics
        and extracurricular development.
      </p>
      <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
        <Card title="Primary Curriculum" description="Foundation skills for young learners." image={gallery2}/>
        <Card title="Secondary Curriculum" description="Advanced subjects and critical thinking." image={gallery2}/>
        <Card title="Clubs & Activities" description="Arts, sports, coding, and more." image={gallery2}/>
      </div>
    </div>
  );
};

export default Academics;
import React from "react";
import Card from "../components/Card";
import { useTranslation } from "react-i18next";
import gallery3 from "../assets/gallery3.jpg";

const News = () => {
  const { t } = useTranslation();
  return (
    <div className="container mx-auto p-8">
      <h1 className="text-4xl font-bold mb-6">{t('news')}</h1>
      <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
        <Card title="Science Fair 2025" description="Students showcased innovative projects." image={gallery3}/>
        <Card title="Annual Sports Day" description="Exciting competitions and awards." image={gallery3}/>
        <Card title="Art & Culture Festival" description="Celebrating creativity and diversity." image={gallery3}/>
        <Card title="Debate Championship" description="Students excelled in public speaking." image={gallery3}/>
      </div>
    </div>
  );
};

export default News;
import React from "react";
import { useTranslation } from "react-i18next";

const Events = () => {
  const { t } = useTranslation();
  return (
    <div className="container mx-auto p-8">
      <h1 className="text-4xl font-bold mb-6">{t('events')}</h1>
      <ul className="list-disc list-inside">
        <li>Science Fair - March 15, 2025</li>
        <li>Annual Sports Day - April 10, 2025</li>
        <li>Art & Culture Festival - May 20, 2025</li>
        <li>Debate Championship - June 5, 2025</li>
        <li>Graduation Ceremony - July 30, 2025</li>
      </ul>
    </div>
  );
};

export default Events;
import React from "react";
import Card from "../components/Card";
import { useTranslation } from "react-i18next";
import gallery1 from "../assets/gallery1.jpg";
import gallery2 from "../assets/gallery2.jpg";
import gallery3 from "../assets/gallery3.jpg";

const Gallery = () => {
  const { t } = useTranslation();
  const images = [gallery1, gallery2, gallery3];
  return (
    <div className="container mx-auto p-8">
      <h1 className="text-4xl font-bold mb-6">{t('gallery')}</h1>
      <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
        {images.map((img, index) => (
          <Card key={index} title={`Gallery ${index+1}`} description="TIPS SCHOOL event" image={img}/>
        ))}
      </div>
    </div>
  );
};

export default Gallery;
import React, { useState } from "react";
import { useTranslation } from "react-i18next";

const Contact = () => {
  const { t } = useTranslation();
  const [form, setForm] = useState({ name: "", email: "", message: "" });

  const handleChange = e => setForm({ ...form, [e.target.name]: e.target.value });
  const handleSubmit = e => {
    e.preventDefault();
    alert(`Thank you, ${form.name}! Your message has been sent.`);
    setForm({ name: "", email: "", message: "" });
  };

  return (
    <div className="container mx-auto p-8">
      <h1 className="text-4xl font-bold mb-6">{t('contact')}</h1>
      <form onSubmit={handleSubmit} className="max-w-md mx-auto space-y-4">
        <input type="text" name="name" value={form.name} onChange={handleChange} placeholder="Name" className="w-full p-2 border rounded"/>
        <input type="email" name="email" value={form.email} onChange={handleChange} placeholder="Email" className="w-full p-2 border rounded"/>
        <textarea name="message" value={form.message} onChange={handleChange} placeholder="Message" className="w-full p-2 border rounded"/>
        <button type="submit" className="bg-blue-900 text-white px-4 py-2 rounded hover:bg-blue-700">Send</button>
      </form>
      <div className="mt-8 text-center">
        <p>Phone: +92-300-XXXXXXX</p>
        <p>Email: info@tipsschool.edu.pk</p>
        <p>Address: 123 School Street, City, Country</p>
      </div>
    </div>
  );
};

export default Contact;
npm install
npm run dev
