<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>U.E.N.A. MPS - Educación de Adultos</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Firebase SDK (Compat v9) -->
    <script src="https://www.gstatic.com/firebasejs/9.22.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.22.0/firebase-firestore-compat.js"></script>
    <!-- QRCode Generator & Library -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/jsqr@1.4.0/dist/jsQR.min.js"></script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Plus Jakarta Sans', sans-serif; }
        @media print {
            body * { visibility: hidden; }
            #printable-card, #printable-card * { visibility: visible; }
            #printable-card { position: absolute; left: 0; top: 0; width: 100%; }
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 min-h-screen flex flex-col">

    <!-- Header Institucional -->
    <header class="bg-indigo-900 text-white shadow-lg">
        <div class="max-w-7xl mx-auto px-4 py-4 flex flex-col sm:flex-row justify-between items-center gap-4">
            <div class="flex items-center gap-3">
                <!-- Escudo SVG Institucional -->
                <svg class="w-12 h-12 text-amber-400" viewBox="0 0 24 24" fill="currentColor">
                    <path d="M12 2L1 7l11 5 9-4.09V17h2V7L12 2zm0 8.5L3.5 7 12 3.15 20.5 7 12 10.5zM3 19v-9.15l9 4.09 9-4.09V19H3z"/>
                </svg>
                <div>
                    <h1 class="text-xl font-bold tracking-wide">U.E.N.A. MPS</h1>
                    <p class="text-xs text-amber-300 font-medium">Educación de Adultos • Sistema de Control y Carnetización</p>
                </div>
            </div>
            
            <div class="flex items-center gap-3">
                <span id="sync-status" class="text-xs bg-emerald-800 text-emerald-100 px-3 py-1 rounded-full font-medium flex items-center gap-1.5">
                    <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span> Conectado en la Nube
                </span>
                <div id="auth-controls">
                    <button onclick="openLoginModal()" id="btn-login-trigger" class="bg-amber-500 hover:bg-amber-600 text-slate-950 font-semibold px-4 py-2 rounded-xl text-sm transition shadow">
                        🔒 Acceso Docente
                    </button>
                    <button onclick="logoutTeacher()" id="btn-logout" class="hidden bg-rose-600 hover:bg-rose-700 text-white font-semibold px-4 py-2 rounded-xl text-sm transition shadow">
                        🔓 Salir Docente
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Navegación por Pestañas -->
    <nav class="bg-white border-b border-slate-200 shadow-sm sticky top-0 z-20">
        <div class="max-w-7xl mx-auto flex overflow-x-auto px-4">
            <button onclick="switchTab('carnets')" id="tab-carnets" class="py-3 px-5 border-b-2 font-semibold text-sm transition border-indigo-600 text-indigo-600 whitespace-nowrap">
                🪪 Carnets Estudiantiles
            </button>
            <button onclick="switchTab('asistencia')" id="tab-asistencia" class="py-3 px-5 border-b-2 font-semibold text-sm transition border-transparent text-slate-500 hover:text-indigo-600 whitespace-nowrap">
                📋 Pase de Lista & Asistencia
            </button>
            <button onclick="switchTab('reportes')" id="tab-reportes" class="py-3 px-5 border-b-2 font-semibold text-sm transition border-transparent text-slate-500 hover:text-indigo-600 whitespace-nowrap">
                📊 Listados por Materia
            </button>
        </div>
    </nav>

    <!-- Contenido Principal -->
    <main class="flex-grow max-w-7xl w-full mx-auto p-4 sm:p-6">

        <!-- SECCIÓN 1: CARNETS -->
        <section id="section-carnets" class="space-y-6">
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                <!-- Formulario de Registro -->
                <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200 lg:col-span-1 space-y-4">
                    <h2 class="text-lg font-bold text-slate-900 border-b pb-2">Registro de Estudiante</h2>
                    
                    <div>
                        <label class="block text-xs font-bold text-slate-600 uppercase mb-1">Nombre Completo</label>
                        <input type="text" id="reg-nombre" placeholder="Ej. María Pérez" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 text-sm">
                    </div>

                    <div>
                        <label class="block text-xs font-bold text-slate-600 uppercase mb-1">Cédula de Identidad</label>
                        <input type="text" id="reg-cedula" placeholder="Ej. V-15234567" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 text-sm">
                    </div>

                    <div>
                        <label class="block text-xs font-bold text-slate-600 uppercase mb-1">Periodo Escolar / Nivel</label>
                        <select id="reg-periodo" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 focus:ring-2 focus:ring-indigo-500 text-sm bg-white">
                            <option value="Primer Periodo">Primer Periodo</option>
                            <option value="Segundo Periodo">Segundo Periodo</option>
                            <option value="Tercer Periodo">Tercer Periodo</option>
                            <option value="Cuarto Periodo">Cuarto Periodo</option>
                            <option value="Quinto Periodo">Quinto Periodo</option>
                            <option value="Sexto Periodo">Sexto Periodo</option>
                        </select>
                    </div>

                    <div>
                        <label class="block text-xs font-bold text-slate-600 uppercase mb-1">Fotografía del Alumno</label>
                        <div class="flex gap-2 mb-2">
                            <input type="file" id="reg-foto-file" accept="image/*" class="hidden" onchange="loadPhotoFile(event)">
                            <button type="button" onclick="document.getElementById('reg-foto-file').click()" class="flex-1 bg-slate-100 hover:bg-slate-200 text-slate-700 py-2 rounded-xl text-xs font-semibold transition border border-slate-300">📁 Galería</button>
                            <button type="button" onclick="startCamera()" class="flex-1 bg-indigo-50 hover:bg-indigo-100 text-indigo-700 py-2 rounded-xl text-xs font-semibold transition border border-indigo-200">📸 Cámara</button>
                        </div>
                        <div id="camera-container" class="hidden relative rounded-xl overflow-hidden bg-black aspect-video mb-2">
                            <video id="video" autoplay playsinline class="w-full h-full object-cover"></video>
                            <button type="button" onclick="takeSnapshot()" class="absolute bottom-2 left-1/2 -translate-x-1/2 bg-white text-slate-900 font-bold px-4 py-1.5 rounded-full text-xs shadow-lg">Capturar Foto</button>
                        </div>
                        <canvas id="canvas" class="hidden"></canvas>
                    </div>

                    <button onclick="registerStudent()" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 rounded-xl transition shadow-md text-sm">
                        Registrar y Generar Carnet
                    </button>
                </div>

                <!-- Vista Previa del Carnet -->
                <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200 lg:col-span-2 flex flex-col items-center justify-center">
                    <h2 class="text-sm font-bold text-slate-500 uppercase tracking-wider mb-4 self-start">Vista Previa del Carnet Digital</h2>
                    
                    <!-- Tarjeta Carnet Imprimible -->
                    <div id="printable-card" class="w-full max-w-sm bg-gradient-to-b from-indigo-950 to-slate-900 text-white rounded-3xl p-6 shadow-2xl border-4 border-amber-400/80 relative overflow-hidden flex flex-col items-center text-center">
                        <div class="absolute -top-12 -right-12 w-32 h-32 bg-amber-400/10 rounded-full blur-2xl"></div>
                        
                        <!-- Header Carnet -->
                        <div class="flex items-center gap-2 mb-3">
                            <svg class="w-8 h-8 text-amber-400" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M12 2L1 7l11 5 9-4.09V17h2V7L12 2zm0 8.5L3.5 7 12 3.15 20.5 7 12 10.5zM3 19v-9.15l9 4.09 9-4.09V19H3z"/>
                            </svg>
                            <div class="text-left">
                                <h3 class="font-extrabold text-sm tracking-widest text-amber-300 leading-tight">U.E.N.A. MPS</h3>
                                <p class="text-[10px] text-slate-300 font-medium">Educación de Adultos</p>
                            </div>
                        </div>

                        <!-- Foto -->
                        <div class="w-28 h-28 rounded-2xl bg-slate-800 border-2 border-amber-400/60 overflow-hidden shadow-inner my-2 relative">
                            <img id="card-foto" src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=150" class="w-full h-full object-cover" alt="Estudiante">
                        </div>

                        <!-- Datos -->
                        <h3 id="card-nombre" class="text-lg font-bold text-white mt-1">Seleccione un estudiante</h3>
                        <p id="card-cedula" class="text-xs text-amber-300/90 font-semibold tracking-wider">CÉDULA: V-00.000.000</p>
                        <span id="card-periodo" class="inline-block bg-white/10 text-slate-200 text-[11px] px-3 py-0.5 rounded-full mt-1.5 border border-white/10">Periodo</span>

                        <!-- QR -->
                        <div class="mt-4 bg-white p-2 rounded-xl shadow">
                            <div id="card-qrcode" class="w-24 h-24 flex items-center justify-center"></div>
                        </div>
                        <p class="text-[9px] text-slate-400 mt-2">Carnet Oficial Verificable</p>
                    </div>

                    <!-- Opciones de Descarga / Impresión -->
                    <div class="mt-6 w-full max-w-sm flex flex-col sm:flex-row gap-3">
                        <select id="export-action-select" class="flex-1 px-3 py-2.5 rounded-xl border border-slate-300 bg-white text-xs font-semibold text-slate-700 shadow-sm">
                            <option value="pdf">Guardar como PDF</option>
                            <option value="print">Imprimir Carnet</option>
                        </select>
                        <button onclick="executeCardExport()" class="bg-slate-900 hover:bg-slate-800 text-white font-bold px-5 py-2.5 rounded-xl text-xs transition shadow">
                            Ejecutar Acción
                        </button>
                    </div>

                    <!-- Lista Rápida de Alumnos -->
                    <div class="mt-8 w-full">
                        <h3 class="text-xs font-bold text-slate-500 uppercase tracking-wider mb-3">Estudiantes Registrados en la Nube</h3>
                        <div id="students-list-container" class="space-y-2 max-h-48 overflow-y-auto pr-2">
                            <!-- Se carga dinámicamente -->
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- SECCIÓN 2: ASISTENCIA (Protegida) -->
        <section id="section-asistencia" class="hidden space-y-6">
            <div id="lock-screen-asistencia" class="bg-white p-10 rounded-2xl shadow-sm border border-slate-200 text-center max-w-md mx-auto space-y-4">
                <div class="w-16 h-16 bg-amber-100 text-amber-600 rounded-2xl flex items-center justify-center mx-auto text-2xl font-bold">🔒</div>
                <h3 class="text-lg font-bold text-slate-900">Módulo Protegido para Docentes</h3>
                <p class="text-xs text-slate-500">Ingrese la clave de acceso de profesor para habilitar el pase de lista y el escáner.</p>
                <button onclick="openLoginModal()" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-2.5 rounded-xl text-sm transition">Ingresar Clave</button>
            </div>

            <div id="unlocked-screen-asistencia" class="hidden grid grid-cols-1 lg:grid-cols-2 gap-6">
                <!-- Escáner QR de Asistencia -->
                <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200 space-y-4">
                    <h2 class="text-lg font-bold text-slate-900">Escáner de Asistencia QR</h2>
                    <div>
                        <label class="block text-xs font-bold text-slate-600 uppercase mb-1">Seleccionar Materia</label>
                        <select id="attendance-subject" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm bg-white">
                            <option value="Matemáticas">Matemáticas</option>
                            <option value="MTC">MTC</option>
                            <option value="Ciencias">Ciencias</option>
                            <option value="Castellano">Castellano</option>
                        </select>
                    </div>

                    <div class="relative rounded-2xl overflow-hidden bg-slate-900 aspect-video flex items-center justify-center">
                        <video id="qr-video" autoplay playsinline class="w-full h-full object-cover"></video>
                        <div id="qr-scanner-overlay" class="absolute inset-0 border-2 border-dashed border-amber-400/60 m-10 rounded-xl pointer-events-none flex items-center justify-center">
                            <span class="bg-black/60 text-white text-[10px] px-3 py-1 rounded-full">Enfoque el código QR del carnet</span>
                        </div>
                    </div>
                    <button onclick="startQRScanner()" class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-bold py-2.5 rounded-xl text-sm transition shadow">
                        Activar Cámara de Escaneo
                    </button>
                </div>

                <!-- Registro Manual y Transcriptor OCR -->
                <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200 space-y-4">
                    <h2 class="text-lg font-bold text-slate-900">Control Manual y Listas Físicas</h2>
                    <div>
                        <label class="block text-xs font-bold text-slate-600 uppercase mb-1">Seleccionar Estudiante para Asistencia</label>
                        <select id="manual-student-select" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm bg-white mb-3">
                            <!-- Dinámico -->
                        </select>
                        <div class="flex gap-2">
                            <button onclick="markManualAttendance('Presente')" class="flex-1 bg-emerald-600 hover:bg-emerald-700 text-white font-bold py-2.5 rounded-xl text-xs transition">Marcar Presente</button>
                            <button onclick="markManualAttendance('Ausente')" class="flex-1 bg-rose-600 hover:bg-rose-700 text-white font-bold py-2.5 rounded-xl text-xs transition">Marcar Ausente</button>
                        </div>
                    </div>

                    <hr class="my-4">
                    
                    <div>
                        <h3 class="text-xs font-bold text-slate-600 uppercase mb-1">Transcriptor OCR de Listas Físicas</h3>
                        <p class="text-xs text-slate-500 mb-2">Sube una foto de tu lista en papel para procesar asistencia masiva.</p>
                        <input type="file" id="ocr-file" accept="image/*" class="w-full text-xs text-slate-500 file:mr-4 file:py-2 file:px-4 file:rounded-xl file:border-0 file:text-xs file:font-semibold file:bg-indigo-50 file:text-indigo-700 hover:file:bg-indigo-100">
                    </div>
                </div>
            </div>
        </section>

        <!-- SECCIÓN 3: REPORTES Y LISTADOS (Protegida) -->
        <section id="section-reportes" class="hidden space-y-6">
            <div id="lock-screen-reportes" class="bg-white p-10 rounded-2xl shadow-sm border border-slate-200 text-center max-w-md mx-auto space-y-4">
                <div class="w-16 h-16 bg-amber-100 text-amber-600 rounded-2xl flex items-center justify-center mx-auto text-2xl font-bold">🔒</div>
                <h3 class="text-lg font-bold text-slate-900">Módulo Protegido para Docentes</h3>
                <p class="text-xs text-slate-500">Ingrese la clave de profesor para ver los listados consolidados por materia.</p>
                <button onclick="openLoginModal()" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-2.5 rounded-xl text-sm transition">Ingresar Clave</button>
            </div>

            <div id="unlocked-screen-reportes" class="hidden bg-white p-6 rounded-2xl shadow-sm border border-slate-200 space-y-4">
                <div class="flex flex-col sm:flex-row justify-between items-center gap-4">
                    <h2 class="text-lg font-bold text-slate-900">Consolidado de Asistencia por Asignatura</h2>
                    <div class="flex gap-2">
                        <select id="report-subject-filter" onchange="renderReports()" class="px-3.5 py-2 rounded-xl border border-slate-300 text-xs bg-white font-semibold">
                            <option value="Matemáticas">Matemáticas</option>
                            <option value="MTC">MTC</option>
                            <option value="Ciencias">Ciencias</option>
                            <option value="Castellano">Castellano</option>
                        </select>
                        <button onclick="exportCSVReport()" class="bg-emerald-600 hover:bg-emerald-700 text-white font-bold px-4 py-2 rounded-xl text-xs transition shadow">📥 Exportar CSV</button>
                    </div>
                </div>

                <div class="overflow-x-auto">
                    <table class="w-full text-left border-collapse text-xs">
                        <thead>
                            <tr class="bg-slate-100 text-slate-700 border-b">
                                <th class="p-3">Cédula</th>
                                <th class="p-3">Estudiante</th>
                                <th class="p-3">Periodo</th>
                                <th class="p-3">Materia</th>
                                <th class="p-3">Estado</th>
                                <th class="p-3">Fecha / Hora</th>
                            </tr>
                        </thead>
                        <tbody id="reports-table-body">
                            <!-- Dinámico -->
                        </tbody>
                    </table>
                </div>
            </div>
        </section>

    </main>

    <!-- Modal de Acceso Docente -->
    <div id="login-modal" class="fixed inset-0 bg-black/60 z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-sm w-full p-6 shadow-2xl space-y-4">
            <h3 class="text-lg font-bold text-slate-900 text-center">Acceso Restringido Docente</h3>
            <p class="text-xs text-slate-500 text-center">Digite su 
