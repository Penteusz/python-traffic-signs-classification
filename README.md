# Rozpoznawanie Znaków Drogowych przy użyciu Konwolucyjnych Sieci Neuronowych 

Skrypt napisany w języku Python wykorzystuje sieci neuronowe konwolucyjne (CNN) do rozpoznawania znaków drogowych na zdjęciach. 

### Skrypt składa się z następujących sekcji:

1. **Importowanie wymaganych bibliotek**: Importowanie niezbędnych bibliotek takich jak NumPy, Pandas, Matplotlib, OpenCV, TensorFlow, PIL i inne, niezbędnych do przetwarzania obrazów i zadań związanych z uczeniem głębokim.

2. **Funkcje programu**: Definicje funkcji wykorzystywanych do określonych zadań w programie.

3. **Parametry programu**: Parametry wykorzystywane do konfiguracji wykonania programu. \
<b>WAŻNE:</b> Należy wskazać ścieżkę bezwględną do katalogu projektu utworzonego w sekcji [Użycie](#Użycie)

4. **Parametry modelu**: Parametry wykorzystywane do uczenia modelu.

5. **Trening modelu**: Główna część programu służąca do wyuczenia modelu na danych treningowych.
<b>WAŻNE:</b> Jeśli w danej lokalizacji (w podpolderze 'trening' katalogu projektu) istnieje model o danej nazwie, to wykona się kod odpowiedzialny za ocenę jakości modelu na próbce testowej (katalog 'Test')

9. **Testowanie na nowych danych**: Ładowanie zestawu testowego, prognozowanie klas za pomocą wytrenowanego modelu i obliczanie dokładności modelu na danych testowych.

10. **Zapis i wczytywanie modelu**: Zapisanie wytrenowanego modelu do pliku oraz jego wczytanie w celu późniejszego użycia.

11. **Prognozowanie na obrazie użytkownika**: Funkcja, która przyjmuje obraz przesłany przez użytkownika, przetwarza go i przewiduje klasę znaku drogowego za pomocą wytrenowanego modelu.

## Użycie

Aby użyć skryptu w środowisku Windows należy wykonać poniższe kroki w terminalu cmd lub Powershell:

1. Należy utworzyć katalog projektu i skopiować do niego pliki projektu \
<b>mkdir Projekt</b><br>
<b>cd Projekt</b><br>
<b>skopiować pliki projektu : <b>git clone https://github.com/Penteusz/python-traffic-signs-classification.git</b> (wymaga zainstalowania aplikacji git)</b> lub pobrać spakowane pliki (.zip) z repozytorium i je rozpakować w katalogu "Projekt" - zostanie utworzony folder o nazwie "python-traffic-signs-classification" zawierający pliki projektowe
2. Należy wejść do folderu "python-traffic-signs-classification" i utworzyć w nim środowisko wirtualne \
<b> python -m venv .\env\traffic-signs</b><br>
\* Jeśli domyśłnie używana jest inna wersja pythona, należy zainstalować wersję 3.8.x i utworzyć środowisko podając ścieżkę do pliku wykonywalego python w wersji 3.8.x np:
<b>C:\Users\\...\Python\Python38\python.exe -m venv .\env\traffic-signs</b>
3. Należy aktywować środowisko wirtualne \
<b>.\env\traffic-signs\Scripts\activate</b>
4. Zainstalować wymagane biblioteki:\
<b>pip install -r requirements.txt --no-cache-dir</b>
5. Utworzyć kernel, który zostanie użyty do wykonania programu: \
<b>python -m ipykernel install --user --name=traffic-signs</b>
6. Uruchomić jupyter notebook: \
<b>jupyter notebook</b>
7. Po uruchomieniu jupyter notebook w przeglądarce internetowej należy wybrać <b>plik "traffic_signs_recognition"</b>
8. W <b>zakładce "Kernel"</b> w panelu górnym wybrać <b>Change kernel</b> a następnie wskazać <b>traffic-signs</b>
9. W pliku projektu "traffic_signs_recognition.ipynb" w sekcji <b>Parametry programu</b> należy zmodyfikować ścieżkę projektu (bezwzględną) <b>project_path</b>, aby wskazywała na <b>katalog "Projekt\python-traffic-signs-classification"</b>.
10. W celu modyfikacji parametrów dotyczących modelu można dostosowywać parametry modelu tj. epochs, batch size w sekcji <b>Parametry programu</b>

## Uruchomienie programu

Program można wykonywać sekwencyjnie - komórka po komórce - albo w całości wybierając na górnym pasku <b>Cell->Run All</b>

## Wymagania

- Python 3.8
- Biblioteki: numpy, Pillow, Keras, tensorflow, matplotlib, jupyter, ipykernel (dokładna specyfikacja w pliku requirements.txt)

