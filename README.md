// =========================
// WORLD-CLASS ML PORTFOLIO UI (UPGRADED)
// =========================

import { motion } from "framer-motion";
import { Github, Linkedin, Mail } from "lucide-react";

export default function App() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-black via-gray-900 to-black text-white p-6">
      <Header />
      <Hero />
      <Projects />
      <Skills />
      <Contact />
    </div>
  );
}

function Header() {
  return (
    <div className="flex justify-between items-center mb-12">
      <h1 className="text-2xl font-bold bg-gradient-to-r from-purple-400 to-blue-500 text-transparent bg-clip-text">
        Darpan | ML Engineer
      </h1>
      <div className="flex gap-4">
        <Github className="hover:text-purple-400 cursor-pointer" />
        <Linkedin className="hover:text-blue-400 cursor-pointer" />
        <Mail className="hover:text-cyan-400 cursor-pointer" />
      </div>
    </div>
  );
}

function Hero() {
  return (
    <motion.div
      initial={{ opacity: 0, y: 40 }}
      animate={{ opacity: 1, y: 0 }}
      className="mb-20"
    >
      <h2 className="text-5xl font-bold mb-6 bg-gradient-to-r from-purple-400 via-blue-400 to-cyan-400 text-transparent bg-clip-text">
        Designing AI Systems That Scale
      </h2>
      <p className="text-gray-400 max-w-xl text-lg">
        Machine Learning Engineer building production-grade AI systems, RAG pipelines, and intelligent products.
      </p>
    </motion.div>
  );
}

function Projects() {
  const projects = [
    {
      title: "Fraud Detection RAG",
      desc: "Explainable AI system for AML fraud investigation",
    },
    {
      title: "Chess AI Coach",
      desc: "Personalized AI training system for chess players",
    },
    {
      title: "Resume Screening AI",
      desc: "Automated NLP-based hiring assistant",
    },
  ];

  return (
    <div className="mb-20">
      <h3 className="text-3xl font-semibold mb-8">Projects</h3>
      <div className="grid md:grid-cols-3 gap-6">
        {projects.map((p, i) => (
          <motion.div
            key={i}
            whileHover={{ scale: 1.05 }}
            className="bg-gradient-to-br from-gray-800 to-gray-900 p-6 rounded-2xl shadow-xl border border-gray-700 hover:border-purple-500 transition shadow-[0_0_20px_rgba(168,85,247,0.2)]"
          >
            <h4 className="text-xl font-bold mb-2">{p.title}</h4>
            <p className="text-gray-400">{p.desc}</p>
          </motion.div>
        ))}
      </div>
    </div>
  );
}

function Skills() {
  const skills = [
    "Python",
    "Machine Learning",
    "Deep Learning",
    "NLP",
    "LangChain",
    "Vector DB",
    "AWS",
  ];

  return (
    <div className="mb-20">
      <h3 className="text-3xl font-semibold mb-8">Skills</h3>
      <div className="flex flex-wrap gap-3">
        {skills.map((s, i) => (
          <span
            key={i}
            className="bg-gradient-to-r from-purple-500 to-blue-500 px-4 py-2 rounded-full text-sm shadow-md hover:scale-105 transition"
          >
            {s}
          </span>
        ))}
      </div>
    </div>
  );
}

function Contact() {
  return (
    <div className="text-center mt-20">
      <h3 className="text-3xl font-semibold mb-4">Let’s Build Something Great 🚀</h3>
      <p className="text-gray-400 mb-6">
        Open to ML roles, collaborations, and AI product building.
      </p>
      <button className="bg-gradient-to-r from-purple-500 to-blue-500 px-6 py-3 rounded-xl shadow-lg hover:scale-105 transition">
        Contact Me
      </button>
    </div>
  );
}

// =========================
// TAILWIND ADDITION (OPTIONAL)
// =========================
// Add this to tailwind.config.js

/*
export default {
  theme: {
    extend: {
      colors: {
        primary: "#7C3AED",
        secondary: "#06B6D4",
        dark: "#0F172A",
      },
    },
  },
};
*/
