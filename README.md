1. Ważna informacja o plikach modeli:

Pliki checkpointów modeli (.pth) nie są dołączone do tego repozytorium ze względu na ich duży rozmiar.

Zostały one wykluczone, ponieważ:

przekraczają typowe zalecenia dotyczące rozmiaru plików na GitHubie
są generowane podczas treningu
każde uruchomienie treningu tworzy osobne wagi modelu

Jeśli jest taka potrzeba, modele można odtworzyć, uruchamiając skrypt treningowy z odpowiednimi parametrami.


2. Wyniki treningów (podsumowanie w Excelu)

Wszystkie eksperymenty treningowe są zapisane w pliku: training_results.xlsx

Plik zawiera pełne porównanie wszystkich eksperymentów, w tym:

zbiór danych (CIFAR10 / CIFAR100)
batch size
liczba epok
learning rate
optimizer (Adam / SGD)
typ schedulera
wartość dropout
accuracy (train / validation / test)
najlepszy loss walidacyjny

Każdy wiersz odpowiada jednemu uruchomieniu treningu.


3. Interpretacja

Plik Excel służy do analizy wpływu hiperparametrów na wydajność modelu. Zawiera obserwacje dotyczące:
overfittingu i underfittingu
zachowania optymalizatora (Adam vs SGD)
wpływu learning rate i batch size
skuteczności schedulerów


4. Struktura projektu

skrypt treningowy – pipeline uczenia modelu
training_results.xlsx – log eksperymentów
checkpointy modeli (.pth) – generowane lokalnie (NIE są wysyłane na GitHub)
