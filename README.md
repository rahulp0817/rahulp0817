import React from 'react';
import { Code, Cloud, Server, Database } from 'lucide-react';

const GithubProfileReadme = () => {
  const skills = [
    { name: 'Java', icon: <Code color="#007396" size={24} /> },
    { name: 'Python', icon: <Code color="#3776AB" size={24} /> },
    { name: 'AWS Cloud', icon: <Cloud color="#FF9900" size={24} /> },
    { name: 'JavaScript', icon: <Code color="#F7DF1E" size={24} /> },
    { name: 'Express.js', icon: <Server color="#000000" size={24} /> },
    { name: 'Next.js', icon: <Server color="#000000" size={24} /> }
  ];

  return (
    <div className="max-w-4xl mx-auto p-6 bg-white shadow-lg rounded-lg">
      <div className="text-center mb-6">
        <h1 className="text-4xl font-bold text-gray-800 animate-pulse">
          Hi there! I'm a Software Developer 👋
        </h1>
      </div>

      <div className="grid md:grid-cols-2 gap-6">
        <div className="bg-gray-100 p-4 rounded-lg">
          <h2 className="text-2xl font-semibold mb-4 text-gray-700">
            🚀 About Me
          </h2>
          <p className="text-gray-600">
            Passionate software developer with expertise in building scalable and 
            efficient web applications. I love turning complex problems into 
            elegant solutions through code.
          </p>
        </div>

        <div className="bg-gray-100 p-4 rounded-lg">
          <h2 className="text-2xl font-semibold mb-4 text-gray-700">
            💻 Tech Skills
          </h2>
          <div className="flex flex-wrap gap-3">
            {skills.map((skill, index) => (
              <div 
                key={index} 
                className="flex items-center bg-white p-2 rounded-md shadow-sm transition hover:scale-105"
              >
                {skill.icon}
                <span className="ml-2 text-gray-700">{skill.name}</span>
              </div>
            ))}
          </div>
        </div>
      </div>

      <div className="mt-6 text-center">
        <h2 className="text-2xl font-semibold mb-4 text-gray-700">
          🌐 Let's Connect!
        </h2>
        <div className="flex justify-center space-x-4">
          <a 
            href="https://linkedin.com/in/yourprofile" 
            target="_blank" 
            className="bg-blue-500 text-white px-4 py-2 rounded-md hover:bg-blue-600 transition"
          >
            LinkedIn
          </a>
          <a 
            href="https://github.com/yourusername" 
            target="_blank" 
            className="bg-gray-800 text-white px-4 py-2 rounded-md hover:bg-gray-900 transition"
          >
            GitHub
          </a>
        </div>
      </div>
    </div>
  );
};

export default GithubProfileReadme;
