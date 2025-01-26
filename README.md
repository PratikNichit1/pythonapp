live server command
sudo yum install python3-pip python3-virtualenv git -y
git clone https://github.com/PratikNichit1/pythonapp.git
cd pythonapp/
python3 -m venv myenv
source myenv/bin/activate
pip install -r requirements.txt
gunicorn --workers 3 --bind 0.0.0.0:5000 app:app&
