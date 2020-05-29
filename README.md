TrafficSignClassification
======
Celem tego programu jest klasyfikacja rodzaju znaku na podstawie odpowiednio sformatowanego obrazu.

Baza danych, z których korzysta program, zawiera obrazy w następującym formacie:
* obraz przedstawia jeden znak drogowy,
* obraz zawiera ramkę wokół znaku, szerokości około 10% znaku (min. 5px)m
* rozmiary obrazów wahają się od 15 x15 do 250 x 250 px,
* obrazy nie muszą być kwadratami,
* znak niekoniecznie znajduje się w centrum obrazu,

Wymagania
---
Python 3.x  
Biblioteki:
* numpy
* pandas
* matplotlib
* cv2
* tensor flow
* PIL
* os
* sklearn
* keras

Korzystanie z programu
---
Program składa się z dwóch skryptów: _traffic_sign.py_ oraz _gui.py_.  
_traffic_sign.py_ odpowiada za trenowanie modelu, natomiast skrypt _gui.py_ pozwala na korzystanie z wyuczonego modelu przy pomocy GUI.

Dane używane w programie pochodzą z [keggle](https://www.kaggle.com/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign).
Po pobraniu i rozpakowaniu bazy obrazów skrypty należy umieścić we wspólnym folderze.

W celu skorzystania z programu należy na początku uruchomić skrypt _traffic_sign.py_, który wygeneruje plik z nauczonym modelem _my_model.h5_.
Następnie można użyć skryptu _gui.py_. Po uruchomieniu skryptu pokazuje się okienko z przyciskiem "Wybierz obraz".
Po kliknięcia w niego należy wybrać obraz, na którym znajduje się znak drogowy.
Po wybraniu pliku, na środku okna programu wyświetlany jest podgląd wybranego pliku.
Po prawej stronie podglądu obrazu pojawia się przycisk "Klasyfikuj obraz".
Po kliknięciu go, nad podglądem obrazu pojawia się nazwa rozpoznanego znaku.
Możliwe jest ponowne wybranie obrazu poprzez kliknięcie w przycisk "Wybierz obraz"