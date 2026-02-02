# ZADANIA KRYPTOGRAFICZNE

## Zadanie 1
Wygeneruj skrót (hash) dla słowa **integrity** wykorzystując algorytm **SHA384**. 
Otrzymany skrót zakoduj w **Base64** i odeślij do serwera jako plik na endpoint **/zadanie**.

## Zadanie 1 (wariant)
Wygeneruj skrót (hash) dla słowa **softwarecompositionanalysis** wykorzystując algorytm **SHA256**. 
Otrzymany skrót zakoduj w **Base64** i odeślij do serwera jako plik na endpoint **/zadanie**.

---

## Zadanie 2
Wygeneruj parę kluczy asymetrycznych w oparciu o kryptografię krzywych eliptycznych (Elliptic Curve Cryptography) korzystając ze standardowej krzywej **secp521r1**. 
Następnie wyeksportuj klucz publiczny w formacie PEM do pliku i prześlij go na serwer na endpoint **/zadanie**.

---

## Zadanie 3
Pobierz **klucz publiczny RSA udostępniony na serwerze** 🔑, oraz **tekst (słowo) do zaszyfrowania**. 
Używając pobranego klucza publicznego RSA, zaszyfruj tekst z zastosowaniem schematu paddingu PKCS#1 OAEP. 
Wynik szyfrowania zakoduj w formacie **Base64** i wyślij jako plik do serwera na endpoint **/zadanie**.

---

## Zadanie 4
Pobierz **klucz symetryczny** 🔑 oraz **słowo przeznaczone do zaszyfrowania**. 
Zaszyfruj słowo używając algorytmu AES w trybie CFB z kluczem o długości 32 bajtów i IV: **19374b8e782a82577f46563789Bcb7a9**. 
Wynik szyfrowania zakoduj w **Base64** i wyślij jako plik do serwera na endpoint **/zadanie**.

---

## Zadanie 4 (wariant CAMELLIA)
Pobierz **klucz symetryczny** 🔑 oraz **słowo przeznaczone do zaszyfrowania**. 
Zaszyfruj słowo używając algorytmu CAMELLIA w trybie CBC z kluczem o długości 16 bajtów i IV: **cb3f8f98579f44a34eb7919cd4fb1471**. 
Wynik szyfrowania zakoduj w **Base64** i wyślij jako plik do serwera na endpoint **/zadanie**.

---

## Zadanie 5
Złam poniższy skrót (hash), który został wygenerowany przy użyciu algorytmu **MD5**: **874449c6ea4df3a9a8a242bdb20b7966**

Wiadomo, że pierwotnym tekstem wejściowym był 6-cyfrowy kod PIN (ciąg cyfr od **000000** do **999999**). 
Ustal oryginalny PIN łamiąc podany skrót. Następnie prześlij odkryty PIN jako zwykły tekst na serwer na endpoint **/zadanie**.

---

## Zadanie 5 (wariant SHA1)
Złam poniższy skrót (hash), który został wygenerowany przy użyciu algorytmu **SHA1**: 
**721d4a537ae21accfb4686dee863f07d321573b0**

Wiadomo, że pierwotnym tekstem wejściowym był 6-cyfrowy kod PIN (ciąg cyfr od **000000** do **999999**). 
Ustal oryginalny PIN łamiąc podany skrót. Następnie prześlij odkryty PIN jako zwykły tekst na serwer na endpoint **/zadanie**.

---

## Zadanie 6
Pobierz **klucz publiczny GPG** 🔑 oraz **podpisany tym kluczem plik** 📝. 
Zweryfikuj podpis cyfrowy oraz odczytaj podpisane słowo, a następnie odeślij do serwera odcisk klucza oraz podpisane słowo. 
Odpowiedź do serwera odeślij w formacie: **ABCD1234:słowo** (gdzie **ABCD1234** to fingerprint klucza, natomiast **słowo** to podpisane słowo) jako tekst na endpoint **/zadanie**.

---