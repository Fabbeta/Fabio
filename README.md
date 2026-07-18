# Fabio
import React from 'react';

interface ProfileProps {
  name: string;
  age: number;
  role: string;
  experienceYears: number;
  specialty: string;
  skills: string[];
}

const FabioProfile: React.FC = () => {
  const profileData: ProfileProps = {
    name: "Fábio Ribeiro",
    age: 54,
    role: "Docente acadêmico e Especialista em Computação",
    experienceYears: 25,
    specialty: "Robótica",
    skills: ["ML", "CD", "DS", "AR", "VR", "AI", "SQL", "JAVA", "Python"]
  };

  return (
    <div className="p-6 max-w-md mx-auto bg-white rounded-xl shadow-md space-y-4">
      <header className="text-center">
        <h1 className="text-2xl font-bold text-gray-900">Olá!</h1>
        <p className="text-gray-500">Meu nome é <span className="font-semibold">{profileData.name}</span></p>
      </header>
      
      <section className="space-y-2">
        <p className="text-sm text-gray-700">
          Tenho {profileData.age} anos, sou <strong>{profileData.role}</strong> com {profileData.experienceYears} anos de experiência na educação.
        </p>
        <p className="text-sm text-gray-700">
          Possuo especialização em <strong>{profileData.specialty}</strong>.
        </p>
      </section>

      <section>
        <h2 className="text-sm font-semibold text-gray-900 uppercase tracking-wider">Principais Habilidades:</h2>
        <div className="flex flex-wrap gap-2 mt-2">
          {profileData.skills.map((skill, index) => (
            <span 
              key={index} 
              className="px-2.5 py-0.5 rounded-full text-xs font-medium bg-blue-100 text-blue-800"
            >
              {skill}
            </span>
          ))}
        </div>
      </section>
    </div>
  );
};

export default FabioProfile;
