# AgriPrecision - Plataforma de Agricultura de Precisión
Autor: Juan Carlos Arias González (2225007)

AgriPrecision es una aplicación web desarrollada en Python con Flask que permite a los agricultores monitorear, gestionar y optimizar sus cultivos mediante análisis de datos, recomendaciones personalizadas y monitoreo en tiempo real. La plataforma ofrece una interfaz intuitiva para administrar cultivos, visualizar mapas de suelos y recibir alertas automáticas sobre condiciones críticas.

Características
Panel de Control: Resumen de cultivos, alertas recientes y pronósticos del tiempo.
Gestión de Cultivos: Crear, editar y eliminar cultivos, con integración de datos de campos.
Análisis de Datos: Gráficos interactivos (humedad, nutrientes, rendimiento) para evaluar la salud de los cultivos.
Recomendaciones Personalizadas: Sugerencias basadas en análisis de suelos y condiciones del cultivo.
Mapas de Suelos: Visualización geoespacial de campos agrícolas.
Monitoreo en Tiempo Real: Gráficos y alertas automáticas para humedad y temperatura (usando WebSocket).
Panel de Administración: Gestión de usuarios, cultivos y alertas para administradores.
Requisitos
Python 3.8 o superior
Flask 2.0+
Flask-SQLAlchemy
Flask-Login
Flask-SocketIO
Bootstrap 5.3
Font Awesome 6.4
Chart.js 4.4
Dependencias adicionales en requirements.txt
Instalación
Clonar el repositorio:

git clone https://github.com/juanarias/agriprecision.git
cd agriprecision
Crear y activar un entorno virtual:
python -m venv venv
source venv/bin/activate # En Windows: venv\Scripts\activate

instalar dependencias
pip install -r requirements.txt

4.Inicializar la base de datos:
Si usas Flask-Migrate:
flask db init
flask db migrate -m "Inicialización de la base de datos"
flask db upgrade

Crear un usuario administrador:
python
from app import app, db, User
with app.app_context():
... user = User(name="Admin", email="admin@example.com", is_admin=True)
... user.set_password("password")
... db.session.add(user)
... db.session.commit()
exit()

Ejecutar la aplicación:
python app.py

Acceder a la aplicación:

Abre http://localhost:5000 en tu navegador.
Inicia sesión con admin@example.com y contraseña password.

ejemplo
![image](https://github.com/user-attachments/assets/e9390a6e-5473-4ff1-a70b-59710e60b1ff)
![image](https://github.com/user-attachments/assets/a4db221a-510e-40d6-8d06-afa3b5ac112a)
![image](https://github.com/user-attachments/assets/54231141-76c7-4f11-8b9d-3ce1197f5e22)
![image](https://github.com/user-attachments/assets/c9071726-754f-435a-a35e-60d2a4799733)
![image](https://github.com/user-attachments/assets/5598a6dc-aa3e-4d68-a8f9-7cc87c352336)




