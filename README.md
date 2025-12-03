import React from 'react';
import { BrowserRouter as Router, Routes, Route, Link } from 'react-router-dom';

function Home() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-900 p-8">
      <h1 className="text-3xl font-semibold">Aditya A. Sapre</h1>
      <p className="mt-1 text-sm text-gray-600">PhD Candidate (Chemical Engineering) • Penn State</p>
      <div className="mt-2 flex flex-wrap gap-3 text-sm">
        <Link to="/contact" className="underline">✉ Email</Link>
        <a href="https://www.linkedin.com" target="_blank" rel="noreferrer" className="underline">LinkedIn</a>
        <Link to="/publications" className="underline">Google Scholar</Link>
    </div>
      <nav className="mt-4 flex gap-3 text-sm">
        <Link to="/about" className="py-2 px-3 rounded hover:bg-gray-100">About</Link>
        <Link to="/experience" className="py-2 px-3 rounded hover:bg-gray-100">Experience</Link>
        <Link to="/research" className="py-2 px-3 rounded hover:bg-gray-100">Research</Link>
        <Link to="/skills" className="py-2 px-3 rounded hover:bg-gray-100">Skills</Link>
        <Link to="/publications" className="py-2 px-3 rounded hover:bg-gray-100">Publications</Link>
        <Link to="/contact" className="py-2 px-3 rounded bg-slate-800 text-white">Contact</Link>
      </nav>
    </div>
  );
}

function About() {
  return (
    <div className="p-8">
      <h2 className="text-2xl font-medium">About</h2>
      <p className="mt-3 text-gray-700 leading-relaxed">
        Doctoral candidate in Chemical Engineering with a multidisciplinary background spanning formulation and process development, microfluidics, enzyme-powered microswimmers, and materials characterization. Combines hands-on lab experience with strong computational and analytical skills.
      </p>
      <Link to="/" className="mt-4 inline-block text-blue-600 underline">Back to Home</Link>
    </div>
  );
}

function Experience() {
  return (
    <div className="p-8">
      <h2 className="text-2xl font-medium">Experience</h2>
      <p className="mt-3 text-gray-700">Industrial and academic research experience in formulation development, protein studies, microfluidics, and process optimization.</p>
      <Link to="/" className="mt-4 inline-block text-blue-600 underline">Back to Home</Link>
    </div>
  );
}

function Research() {
  return (
    <div className="p-8">
      <h2 className="text-2xl font-medium">Research & Publications</h2>
      <p className="mt-3 text-gray-700">Selected research spanning enzyme-powered transport, chemo‑taxis, programmable fluid motion, and active colloids.</p>

      {/* Example of a paper entry with image and abstract */}
      <div className="mt-6 bg-white p-4 rounded-lg shadow-sm">
        <h3 className="text-lg font-semibold">Non-reciprocal Chemotactic Movement in Enzyme Cascade</h3>
        <img src="/path/to/image1.jpg" alt="Paper 1" className="mt-2 w-full max-w-md rounded shadow" />
        <p className="mt-2 text-gray-700">Abstract: This study demonstrates non-reciprocal chemotactic movement of enzyme cascades under flow-free conditions. The work provides insights into microscale transport mechanisms and enzyme-driven motility.</p>
      </div>

      <div className="mt-6 bg-white p-4 rounded-lg shadow-sm">
        <h3 className="text-lg font-semibold">Hydrogel-Induced Concentration Gradient Generation</h3>
        <img src="/path/to/image2.jpg" alt="Paper 2" className="mt-2 w-full max-w-md rounded shadow" />
        <p className="mt-2 text-gray-700">Abstract: A cautionary perspective on hydrogel-induced gradients and their implications for chemotaxis studies. Highlights the challenges and recommendations for accurate experimental designs.</p>
      </div>

      <Link to="/" className="mt-4 inline-block text-blue-600 underline">Back to Home</Link>
    </div>
  );
}

function Skills() {
  return (
    <div className="p-8">
      <h2 className="text-2xl font-medium">Skills</h2>
      <p className="mt-3 text-gray-700">Technical: AFM, DLS, NTA, SEM, TEM, SAXS/WAXS, FTIR, UV‑Vis, SEC, HPLC. Software: MATLAB, COMSOL, JMP, Excel, L‑Edit, Blender, Photoshop.</p>
      <Link to="/" className="mt-4 inline-block text-blue-600 underline">Back to Home</Link>
    </div>
  );
}

function Publications() {
  return (
    <div className="p-8">
      <h2 className="text-2xl font-medium">Publications</h2>
      <p className="mt-3 text-gray-700">Each publication now has space for an abstract and an image in the Research section.</p>
      <Link to="/" className="mt-4 inline-block text-blue-600 underline">Back to Home</Link>
    </div>
  );
}

function Contact() {
  return (
    <div className="p-8">
      <h2 className="text-2xl font-medium">Contact</h2>
      <p className="mt-3 text-gray-700">Email: your.email@domain.com • Phone: +1‑919‑785‑8427</p>
      <Link to="/" className="mt-4 inline-block text-blue-600 underline">Back to Home</Link>
    </div>
  );
}

export default function App() {
  return (
    <Router>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/experience" element={<Experience />} />
        <Route path="/research" element={<Research />} />
        <Route path="/skills" element={<Skills />} />
        <Route path="/publications" element={<Publications />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </Router>
  );
}

