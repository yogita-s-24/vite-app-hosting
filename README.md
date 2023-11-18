# vite-app-hosting

import path from 'path';

const __dirname = path.resolve();

if (process.env.NODE_ENV === 'production') {
  app.use(express.static(path.join(__dirname, '..', 'client', 'dist')));

  app.get('*', (req, res) => {
    res.sendFile(path.join(__dirname, '..', 'client', 'dist', 'index.html'))
  });
}

// Build Command: cd client && npm install && npm run build && cd .. && cd server && npm install

// Start Command: cd server && npm start
