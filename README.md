# notes
% Dostępne kolory
color(green).
color(red).
color(blue).

% Sprawdza czy dwa kolory są różne
different_colors(C1, C2) :-
    color(C1),
    color(C2),
    C1 \= C2.

% Główny predykat rozwiązujący problem kolorowania
% Dla każdego wierzchołka przypisujemy kolor
% i sprawdzamy ograniczenia dla każdej krawędzi
solve_coloring :-
    % Przypisz kolory do wierzchołków
    color(A), color(B), color(C), color(D), color(E),
    
    % Sprawdź ograniczenia dla każdej krawędzi
    different_colors(A, B),  % krawędź A-B
    different_colors(A, C),  % krawędź A-C
    different_colors(B, C),  % krawędź B-C
    different_colors(B, D),  % krawędź B-D
    different_colors(C, D),  % krawędź C-D
    different_colors(D, E),  % krawędź D-E
    
    % Wyświetl rozwiązanie
    format('Rozwiązanie:~n'),
    format('A = ~w~n', [A]),
    format('B = ~w~n', [B]),
    format('C = ~w~n', [C]),
    format('D = ~w~n', [D]),
    format('E = ~w~n', [E]).

lengthList :: [Int] -> Int
lengthList [] = 0
lengthList (_:xs) = 1 + lengthList xs

module Main where

-- Funkcja spłaszczająca listę list
flatten :: [[Int]] -> [Int]
flatten [] = []
flatten (x:xs) = x ++ flatten xs

main :: IO ()
main = do
    putStrLn "Testy funkcji flatten:"
    putStrLn $ "flatten [[1,2,3], [4,5], [6]] = " ++ show (flatten [[1,2,3], [4,5], [6]])
    putStrLn $ "flatten [[], [], []] = " ++ show (flatten [[], [], []])
    putStrLn $ "flatten [[10,20], [30]] = " ++ show (flatten [[10,20], [30]])
    putStrLn $ "flatten [] = " ++ show (flatten [])
    putStrLn $ "flatten [[1], [2], [3]] = " ++ show (flatten [[1], [2], [3]])

    module Main where

-- Funkcja obliczająca długość listy
lengthList :: [Int] -> Int
lengthList [] = 0
lengthList (_:xs) = 1 + lengthList xs

main :: IO ()
main = do
    putStrLn "Testy funkcji lengthList:"
    putStrLn $ "lengthList [1,2,3,4,5] = " ++ show (lengthList [1,2,3,4,5])
    putStrLn $ "lengthList [] = " ++ show (lengthList [])
    putStrLn $ "lengthList [10,20,30] = " ++ show (lengthList [10,20,30])
    putStrLn $ "lengthList [1] = " ++ show (lengthList [1])
    putStrLn $ "lengthList [1..100] = " ++ show (lengthList [1..100])
