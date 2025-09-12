# 6obcy TUI Chat Bot

Terminalowy klient do [6obcy.org](https://6obcy.org) z obsługą:
- anonimowych rozmów z losowymi osobami,
- automatycznych odpowiedzi generowanych przez AI (DeepSeek),
- rozwiązywania captcha przy pomocy 2captcha,
- prostego TUI (Text User Interface) opartego o `neo-blessed`.

## ✨ Funkcje

- ✅ Łączenie z serwerem 6obcy przez WebSocket  
- ✅ Interfejs w terminalu (`neo-blessed`)  
- ✅ Historia wiadomości i scrollowanie  
- ✅ Obsługa captcha:
  - ręczne przepisywanie kodu,
  - lub automatyczne rozwiązywanie przez 2captcha API  
- ✅ Tryb auto-odpowiedzi (AI odpowiada za Ciebie)  
- ✅ Licznik osób online  
- ✅ Komendy `/topic`, `/dis`, `/start`, `/stop`, `/auto`  

---

## 🚀 Instalacja

1. Sklonuj repozytorium i zainstaluj zależności:

```bash
git clone https://github.com/twoj-user/6obcy-bot.git
cd 6obcy-bot
npm install
```

2. Utwórz plik `.env` z wymaganymi kluczami:

```env
DEEPSEEK_API_KEY=twój_klucz_od_deepseek
CAPTCHA2_API=twój_klucz_od_2captcha   # opcjonalnie
WELCOME=hejka 👋                      # opcjonalna wiadomość powitalna
```

---

## ▶️ Uruchamianie

```bash
npm start
```

Po uruchomieniu:
- aplikacja łączy się z serwerem 6obcy,
- jeśli pojawi się captcha, otworzy się strona `http://localhost:<port>/captcha`,  
- można pisać wiadomości w dolnym polu terminala.

---

## 💻 Sterowanie

- `/topic` → losowe pytanie od serwera  
- `/dis` → rozłącz  
- `/start` → rozpocznij rozmowę  
- `/stop` → zakończ rozmowę i wyłącz auto-reconnect  
- `/auto` → włącz/wyłącz auto-odpowiedzi AI  
- `Esc` lub `Ctrl+C` → zakończ program  

---

## ⚠️ Uwaga

- Używanie botów na 6obcy.org może być sprzeczne z regulaminem. Ten projekt służy wyłącznie do celów edukacyjnych i testowych.  
- Nie udostępniaj swojego klucza API publicznie.  

---

## 🛠️ Stos technologiczny

- [Node.js](https://nodejs.org/)  
- [WebSocket](https://www.npmjs.com/package/ws)  
- [neo-blessed](https://github.com/chjj/blessed)  
- [ora](https://www.npmjs.com/package/ora)  
- [colors](https://www.npmjs.com/package/colors)  
- [express](https://expressjs.com/)  
- [DeepSeek API](https://deepseek.com)  
- [2captcha API](https://2captcha.com/)  
