# Plan-de-Estudios---CP
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Malla Curricular - Contador Público</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Malla Curricular - Contador Público</h1>

  <div class="year" id="primer">
    <h2>Primer Año</h2>
    <div class="subjects">
      <div class="subject" onclick="showInfo('CR001')">Introducción a la Matemática</div>
      <div class="subject" onclick="showInfo('CR002')">Introducción a las Ciencias Económicas</div>
      <div class="subject" onclick="showInfo('CR101')">Introducción al Conocimiento Científico</div>
      <div class="subject" onclick="showInfo('CR102')">Administración I</div>
      <div class="subject" onclick="showInfo('CR103')">Álgebra</div>
      <div class="subject" onclick="showInfo('CR104')">Introducción a la Contabilidad</div>
      <div class="subject" onclick="showInfo('CR105')">Análisis Matemático</div>
      <div class="subject" onclick="showInfo('CR106')">Microeconomía I</div>
    </div>
  </div>

  <!-- Podés seguir copiando el mismo patrón para Segundo Año, Tercer Año, etc. -->

  <div id="infoBox" class="info-box" style="display: none;">
    <span id="closeBtn" onclick="hideInfo()">×</span>
    <h3 id="subjectTitle"></h3>
    <p><strong>Código:</strong> <span id="subjectCode"></span></p>
    <p><strong>Correlatividades:</strong> <span id="subjectReqs"></span></p>
  </div>

  <script src="script.js"></script>
</body>
</html>
body {
  background-color: #fdf6e3;
  font-family: 'Segoe UI', sans-serif;
  margin: 0;
  padding: 20px;
  color: #333;
}

h1 {
  text-align: center;
  color: #3e4e40;
}

.year {
  margin-bottom: 40px;
}

.year h2 {
  background-color: #a88c6f;
  color: white;
  padding: 10px;
  border-radius: 5px;
}

.subjects {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 10px;
}

.subject {
  background-color: #ffffff;
  border: 2px solid #3e4e40;
  padding: 10px 15px;
  border-radius: 6px;
  cursor: pointer;
  transition: 0.3s;
}

.subject:hover {
  background-color: #e0ddce;
}

.info-box {
  position: fixed;
  top: 30%;
  left: 50%;
  transform: translate(-50%, -30%);
  background-color: #fff;
  padding: 20px;
  border: 2px solid #3e4e40;
  border-radius: 8px;
  box-shadow: 0px 0px 10px #999;
  width: 300px;
  z-index: 1000;
}

#closeBtn {
  float: right;
  cursor: pointer;
  font-weight: bold;
  font-size: 20px;
  color: #800000;
}
const materias = {
  "CR001": {
    nombre: "Introducción a la Matemática",
    correlativas: "Ninguna"
  },
  "CR002": {
    nombre: "Introducción a las Ciencias Económicas",
    correlativas: "Ninguna"
  },
  "CR101": {
    nombre: "Introducción al Conocimiento Científico",
    correlativas: "CR002"
  },
  "CR102": {
    nombre: "Administración I",
    correlativas: "CR002"
  },
  "CR103": {
    nombre: "Álgebra",
    correlativas: "CR001"
  },
  "CR104": {
    nombre: "Introducción a la Contabilidad",
    correlativas: "CR002"
  },
  "CR105": {
    nombre: "Análisis Matemático",
    correlativas: "CR103"
  },
  "CR106": {
    nombre: "Microeconomía I",
    correlativas: "CR103, CR002"
  }
};

function showInfo(codigo) {
  const materia = materias[codigo];
  if (!materia) return;

  document.getElementById("subjectTitle").textContent = materia.nombre;
  document.getElementById("subjectCode").textContent = codigo;
  document.getElementById("subjectReqs").textContent = materia.correlativas;
  document.getElementById("infoBox").style.display = "block";
}

function hideInfo() {
  document.getElementById("infoBox").style.display = "none";
}
<div class="year" id="segundo">
  <h2>Segundo Año</h2>
  <div class="subjects">
    <div class="subject" onclick="showInfo('CR201')">Contabilidad Intermedia</div>
    <div class="subject" onclick="showInfo('CR202')">Derecho Privado</div>
    <div class="subject" onclick="showInfo('CR203')">Estadística I</div>
    <div class="subject" onclick="showInfo('CR204')">Microeconomía II</div>
    <div class="subject" onclick="showInfo('CR205')">Análisis Matemático II</div>
    <div class="subject" onclick="showInfo('CR206')">Sociología</div>
    <div class="subject" onclick="showInfo('CR207')">Contabilidad de Costos</div>
    <div class="subject" onclick="showInfo('CR208')">Estadística II</div>
  </div>
</div>
  "CR201": {
    nombre: "Contabilidad Intermedia",
    correlativas: "CR104"
  },
  "CR202": {
    nombre: "Derecho Privado",
    correlativas: "CR101"
  },
  "CR203": {
    nombre: "Estadística I",
    correlativas: "CR103"
  },
  "CR204": {
    nombre: "Microeconomía II",
    correlativas: "CR106"
  },
  "CR205": {
    nombre: "Análisis Matemático II",
    correlativas: "CR105"
  },
  "CR206": {
    nombre: "Sociología",
    correlativas: "CR101"
  },
  "CR207": {
    nombre: "Contabilidad de Costos",
    correlativas: "CR104"
  },
  "CR208": {
    nombre: "Estadística II",
    correlativas: "CR203"
  }
  <div class="year" id="tercero">
  <h2>Tercer Año</h2>
  <div class="subjects">
    <div class="subject" onclick="showInfo('CR301')">Macroeconomía</div>
    <div class="subject" onclick="showInfo('CR302')">Matemática Financiera</div>
    <div class="subject" onclick="showInfo('CR303')">Contabilidad Superior</div>
    <div class="subject" onclick="showInfo('CR304')">Derecho Público</div>
    <div class="subject" onclick="showInfo('CR305')">Finanzas Públicas</div>
    <div class="subject" onclick="showInfo('CR306')">Impuestos I</div>
    <div class="subject" onclick="showInfo('CR307')">Administración II</div>
  </div>
</div>
<div class="year" id="cuarto">
  <h2>Cuarto Año</h2>
  <div class="subjects">
    <div class="subject" onclick="showInfo('CR401')">Derecho Laboral</div>
    <div class="subject" onclick="showInfo('CR402')">Auditoría</div>
    <div class="subject" onclick="showInfo('CR403')">Impuestos II</div>
    <div class="subject" onclick="showInfo('CR404')">Finanzas de Empresa</div>
    <div class="subject" onclick="showInfo('CR405')">Administración Pública</div>
    <div class="subject" onclick="showInfo('CR406')">Sistemas Administrativos</div>
    <div class="subject" onclick="showInfo('CR407')">Ética y Deontología Profesional</div>
  </div>
</div>
<div class="year" id="quinto">
  <h2>Quinto Año</h2>
  <div class="subjects">
    <div class="subject" onclick="showInfo('CR501')">Práctica Profesional Supervisada</div>
    <div class="subject" onclick="showInfo('CR502')">Seminario de Integración y Evaluación Final</div>
  </div>
</div>
  // Tercer Año
  "CR301": {
    nombre: "Macroeconomía",
    correlativas: "CR106"
  },
  "CR302": {
    nombre: "Matemática Financiera",
    correlativas: "CR205"
  },
  "CR303": {
    nombre: "Contabilidad Superior",
    correlativas: "CR201"
  },
  "CR304": {
    nombre: "Derecho Público",
    correlativas: "CR202"
  },
  "CR305": {
    nombre: "Finanzas Públicas",
    correlativas: "CR106"
  },
  "CR306": {
    nombre: "Impuestos I",
    correlativas: "CR201"
  },
  "CR307": {
    nombre: "Administración II",
    correlativas: "CR102"
  },

  // Cuarto Año
  "CR401": {
    nombre: "Derecho Laboral",
    correlativas: "CR202"
  },
  "CR402": {
    nombre: "Auditoría",
    correlativas: "CR303"
  },
  "CR403": {
    nombre: "Impuestos II",
    correlativas: "CR306"
  },
  "CR404": {
    nombre: "Finanzas de Empresa",
    correlativas: "CR302"
  },
  "CR405": {
    nombre: "Administración Pública",
    correlativas: "CR305"
  },
  "CR406": {
    nombre: "Sistemas Administrativos",
    correlativas: "CR307"
  },
  "CR407": {
    nombre: "Ética y Deontología Profesional",
    correlativas: "CR303"
  },

  // Quinto Año
  "CR501": {
    nombre: "Práctica Profesional Supervisada",
    correlativas: "80% de la carrera"
  },
  "CR502": {
    nombre: "Seminario de Integración y Evaluación Final",
    correlativas: "CR501"
  }
  
