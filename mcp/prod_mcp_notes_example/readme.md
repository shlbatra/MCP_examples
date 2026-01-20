Run backend locally - This runs fastmcp server locally with notes app
uv run main.py

NGROK - Sets up local fastmcp to public url that works with claude code
Provides public address to mcp server
ngrok config add-authtoken <token>
ngrok http 8000
Ex. Forwarding                    https://clarisa-unirascible-salena.ngrok-free.dev -> http://localhost:8000

Add mcp server to claude
claude mcp add --transport http notes https://clarisa-unirascible-salena.ngrok-free.dev/mcp


Stytch for authentication mcp with user credentials provided in Stytch
Connected Apps -> Settings -> Enable dynamic client registration -> Add Authorization URL -> http://localhost:5173
URL above in prod will be hosted. Open URL for login via Frontend.


Steps to create react project for front end
npm craeate vite@latest --frontend
React framework with Javascript
rm -rf node_modules package-lock.json                                                                                                                                        
npm install                                                                                                                                                                  
npm install @stytch/react 
npm install @stytch/vanilla-js

Run front end with 
npm run dev
localhost:5173

Finally test everything in claude code.