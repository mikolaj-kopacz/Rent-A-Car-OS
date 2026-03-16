# 🚗 Rent-A-Car OS

Kompleksowy system do zarządzania wypożyczalnią samochodów, oparty na bazie danych **PostgreSQL** oraz interfejsie w **Python (Streamlit)**. Projekt realizuje pełną obsługę procesów biznesowych: od zarządzania flotą, przez rezerwacje, po raporty finansowe.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15%2B-336791)
![Streamlit](https://img.shields.io/badge/Streamlit-App-FF4B4B)

## 📋 Główne Funkcjonalności

### 🖥️ Panel Menadżera
* **Zarządzanie Flotą:** Dodawanie nowych aut, usuwanie, edycja cennika.
* **Rejestracja Serwisów:** Ewidencja napraw i kosztów.
* **Zarządzanie Personelem:** Dodawanie i usuwanie kont pracowników.
* **Raporty:** Wykresy przychodów i efektywności pracowników.

### 👤 Panel Pracownika
* **Rezerwacje:** Wyszukiwanie dostępnych aut w zadanym terminie.
* **Obsługa Klienta:** Baza CRM, historia wypożyczeń, dodawanie nowych klientów.
* **Szybkie Akcje:** Zgłaszanie usterek, wydawanie i odbiór pojazdów.
* **System Alertów:** Automatyczne powiadomienia o autach wymagających serwisu (na podstawie przebiegu).

## 🛠️ Technologie

* **Baza Danych:** PostgreSQL (PL/pgSQL - procedury składowane, funkcje, triggery).
* **Backend/Frontend:** Python + Streamlit.
* **Biblioteki:** `psycopg2` (połączenie z DB), `pandas` (analiza danych), `fpdf` (generowanie potwierdzeń PDF).

## 🚀 Jak uruchomić projekt?

### Wymagania
* Python 3.8+
* PostgreSQL
* Menedżer pakietów `uv` (opcjonalnie, można użyć standardowego `pip`).

### Instalacja

1.  **Sklonuj repozytorium:**
    ```bash
    git clone [https://github.com/mikolaj-kopacz/rent-a-car-os.git](https://github.com/mikolaj-kopacz/rent-a-car-os.git)
    cd rent-a-car-os
    ```

2.  **Przygotuj Bazę Danych:**
    * Utwórz bazę w PostgreSQL (np. `wypozyczalnia`).
    * Uruchom skrypt `setup.sql` (tworzy tabele i funkcje).
    * Uruchom skrypt `dane.sql` (wgrywa przykładowe dane).

3.  **Skonfiguruj połączenie:**
    * Edytuj plik `src/db.py` i wpisz swoje dane do bazy (host, user, password).

4.  **Zainstaluj zależności i uruchom:**

    **Opcja A (zalecana - uv):**
    ```bash
    uv sync
    uv run streamlit run src/app.py
    ```

    **Opcja B (standardowa - pip):**
    ```bash
    pip install streamlit psycopg2-binary pandas fpdf
    streamlit run src/app.py
    ```

## 🔑 Dane logowania (Demo)

| Rola | Login | Hasło |
| :--- | :--- | :--- |
| **Menadżer** | `admin` | `admin` |
| **Pracownik** | `ewa` | `ewa` |

---
*Projekt zrealizowany w ramach przedmiotu Bazy Danych.*
