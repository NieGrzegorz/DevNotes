Flask applications are built arround requests and responses. 

request - browser does that, communicates with an application placed on a server, server creates response and sends it back 

normally flask application is called app.py 

Flask is a class 

app = Flask(__name__)

flask decorator for route handling: 
@app.route(route) // by default handles GET request

@app.route(route, methods = ["METHOD"])

Syntax for accepting params 

@app.route(route/<string:name>)
def foo(name): 


request package 


Test first design: 
flask_restful -> Resource and Api to import 