# PAGINA-DE-CURSOS
PAGINA DE CURSOS HTML CSS
import React, { useState } from "react";
// import logo from "./image.png"; // Descomentar y agregar el logo aquí

const App = () => {
  const [formData, setFormData] = useState({
    fullName: "",
    username: "",
    email: "",
    phone: "",
    address: "",
    password: ""
  });

  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData({ ...formData, [name]: value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    alert(`Usuario creado con éxito: ${JSON.stringify(formData)}`);
  };

  return (
    <div className="min-h-screen flex items-center justify-center bg-[#f7f7f7]">
      <form
        onSubmit={handleSubmit}
        className="bg-[#ffffff] p-8 rounded-xl shadow-lg w-full max-w-md"
      >
        <div className="flex justify-center mb-6">
          {/* <img src={logo} alt="Logo" className="h-20 w-auto" /> */} {/* Espacio reservado para el logo */}
        </div>
        
        <h1 className="text-2xl font-bold text-center text-[#0000ff] mb-6">
          Crear Usuario
        </h1>

        <div className="mb-4">
          <label className="block text-[#010101] font-semibold mb-2">Nombre Completo:</label>
          <input
            type="text"
            name="fullName"
            value={formData.fullName}
            onChange={handleChange}
            placeholder="Ingrese su nombre completo"
            className="w-full p-3 border rounded-xl focus:outline-none focus:ring-2 focus:ring-[#0000ff]"
          />
        </div>

        <div className="mb-4">
          <label className="block text-[#010101] font-semibold mb-2">Nombre de Usuario:</label>
          <input
            type="text"
            name="username"
            value={formData.username}
            onChange={handleChange}
            placeholder="Ingrese su nombre de usuario"
            className="w-full p-3 border rounded-xl focus:outline-none focus:ring-2 focus:ring-[#0000ff]"
          />
        </div>

        <div className="mb-4">
          <label className="block text-[#010101] font-semibold mb-2">Correo Electrónico:</label>
          <input
            type="email"
            name="email"
            value={formData.email}
            onChange={handleChange}
            placeholder="Ingrese su correo electrónico"
            className="w-full p-3 border rounded-xl focus:outline-none focus:ring-2 focus:ring-[#0000ff]"
          />
        </div>

        <div className="mb-4">
          <label className="block text-[#010101] font-semibold mb-2">Teléfono:</label>
          <input
            type="tel"
            name="phone"
            value={formData.phone}
            onChange={handleChange}
            placeholder="Ingrese su número de teléfono"
            className="w-full p-3 border rounded-xl focus:outline-none focus:ring-2 focus:ring-[#0000ff]"
          />
        </div>

        <div className="mb-4">
          <label className="block text-[#010101] font-semibold mb-2">Dirección:</label>
          <input
            type="text"
            name="address"
            value={formData.address}
            onChange={handleChange}
            placeholder="Ingrese su dirección"
            className="w-full p-3 border rounded-xl focus:outline-none focus:ring-2 focus:ring-[#0000ff]"
          />
        </div>

        <div className="mb-6">
          <label className="block text-[#010101] font-semibold mb-2">Contraseña:</label>
          <input
            type="password"
            name="password"
            value={formData.password}
            onChange={handleChange}
            placeholder="Ingrese su contraseña"
            className="w-full p-3 border rounded-xl focus:outline-none focus:ring-2 focus:ring-[#0000ff]"
          />
        </div>

        <button
          type="submit"
          className="w-full bg-[#ff0000] text-white py-3 rounded-xl hover:bg-[#010101] transition"
        >
          Crear Usuario
        </button>
      </form>
    </div>
  );
};

export default App;
