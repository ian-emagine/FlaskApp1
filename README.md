# FlaskApp1

Flask app created in Windows 10 environment on Visual Studio Code using Powershell terminal.

Original location is user directors of Windows user

Installed pip
python -m pip install --upgrade pip

Created new environment
python -m venv myenv

Installed then upgraded Flask
pip install flask
pip install flask --upgrade flask

Made then entered new project directory
md todo_service_flask
cd todo_service_flask

Created main.py
New-item helper.py -ItemType file

Created helper.py
New-item helper.py -ItemType file

Changed location back to to user directors
cd ..

Activate environment
.\myenv\Scripts\Activate.ps1

Changed location to project directory
cd todo_service_flask

Set environemt variable for FLASK_APP
$env:FLASK_APP = "main.py"

Run Flask
flask run

Opened new terminal then ran curl on the root path (/) to ensure server was running
curl.exe -X POST http://127.0.0.1:5000/

Then ran the path to add a new item using curl
curl.exe -X POST http://127.0.0.1:5000/item/new -d '{\"item\": \"Setting up Flask\"}' -H "Content-Type: application/json"

The position of the quotes are important in Windows. It will cause an error otherwise.

This returned the expected response
{"item": "Setting up Flask", "status": "Not Started"}



