# Instalare WordPress

## Cerințe și acces

- **Versiunea minimă PHP:** 8.3
- **cPanel:** sunt necesare datele de autentificare (utilizator și parolă).
- **WordPress Admin:** păstrați datele de autentificare (utilizator și parolă) într-un loc sigur.

> Nu salvați parole sau chei API în acest fișier. Completați-le printr-un canal securizat la momentul configurării.

## Instalarea fișierelor

1. Încărcați `wp-content.zip` pe server.
2. Dezarhivați-l și permiteți înlocuirea fișierelor existente.

## Configurarea WordPress

- Activați pluginurile necesare.
- Configurați biblioteca media să nu creeze foldere pe lună/an.
- Adăugați categoria **Articole**.

## Google Drive

- Spațiu recomandat: **1.500 MB**; de preferat să existe deja un cont Google Drive.
- **Folderul Monitorului Oficial:** ID-ul folderului trebuie completat pentru locația Drive asociată domeniului `primariabebaveche.ro`.
- **API Google Drive:** configurarea se face în [Google Cloud Console](https://console.cloud.google.com/).
- Pentru salvarea directă pe server, folosiți locația `/wp-content/upload/formulare` (confirmați calea exactă înainte de configurare).

## Publicarea articolelor prin e-mail (Postie)

Configurați pluginul **Postie** cu IMAP prin SSL, portul **993**, fără corectare de timp.

### Variante de e-mail

- **Gmail:** `imap.gmail.com` — notează utilizatorul `brwb8w5a@gmail.com`; parola trebuie introdusă separat și păstrată securizat.
- **E-mail intern recomandat:** `wp@primariabebaveche.ro`, server `mail.primariabebaveche.ro`; parola trebuie introdusă separat și păstrată securizat.

### Setări de publicare

- Configurați lista adreselor de e-mail autorizate să publice. Administratorul site-ului WordPress este deja autorizat.
- E-mailurile cu titlul care începe cu `[public]` sunt publicate direct pe prima pagină.
- **Utilizator implicit pentru postări:** `admin`
- **Categorie implicită:** `Articole`

## Sincronizarea fișierelor

1. Instalați **FreeFileSync**.
2. Alegeți folderul local pentru sincronizarea Monitorului Oficial; folderele din arhiva `foldere.zip` sunt deja pregătite.
3. În FreeFileSync, configurați folderul local și folderul online. Pentru locația online, folosiți opțiunea FTP (pictograma nor din dreapta, conform notițelor inițiale).
4. Salvați configurația ca fișier **batch** pe Desktop.
5. Faceți dublu clic pe fișierul batch pentru a porni încărcarea.
