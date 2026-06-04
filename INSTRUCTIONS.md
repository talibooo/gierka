# Gierka

Masz 3 realne drogi. Wybor zalezy od tego, czy chcesz szybki prototyp, czy "prawdziwa" gre Android.

## Opcja A (najprostsza): Python + Kivy + Buildozer

Najlepsza do startu.

### 1. Instalacja srodowiska (PC Linux / WSL)

Na Windows najlatwiej WSL (Ubuntu).

sudo apt update
sudo apt install python3 python3-pip git -y
pip install kivy buildozer

### 2. Tworzenie projektu

mkdir deadland
cd deadland
buildozer init

### 3. Minimalna gra (main.py)

from kivy.app import App
from kivy.uix.label import Label

class Game(App):
    def build(self):
        return Label(text="Deadland Survival")

Game().run()

### 4. Build Android APK

buildozer -v android debug

Na koncu dostajesz plik .apk.

## Opcja B (lepsza gra): Godot Engine

Jesli chcesz cos jak DayZ w 2.5D.

### Co dostajesz:
- gotowy silnik
- multiplayer wbudowany
- animacje, kolizje, mapa
- eksport na Androida

### Kroki:
1. Pobierz Godot: https://godotengine.org
2. Nowy projekt 2D
3. Izometryczna siatka
4. Skrypty w GDScript (Python-like)
5. Export Android SDK

## Opcja C (pro, trudna): Unity

Najbardziej AAA, ale ciezkie.

# Co robisz TERAZ (konkretnie)

Jesli chcesz isc w Twoja gre (DayZ-like):

1. Powiedz: "Kivy" albo "Godot"
2. Zaczynamy od:
- ruch postaci
- mapa
- kamera izometryczna
- zombie AI

## Wazne (bez sciemy)

Twoja gra jest:
- duza (multiplayer + survival + open world)
- nie do zrobienia od razu

Musimy ja zbudowac etapami:
1. ruch + kamera
2. jedna mapa
3. zombie
4. walka
5. survival (glod, pragnienie)
6. crafting
7. multiplayer
