# haskell
listaExercicio

soma :: Int -> Int -> Int
soma a b = a+b

somaList:: [Int] -> Int 
somaList [] = 0
somaList (a:as) = a + somaList as

subtracao :: Int->Int -> Int
subtracao a b = a - b

subtracaoList :: [Int] -> Int 
subtracaoList [] = 0
subtracaoList(a:as) = a - somaList as

multiplicacao :: Int-> Int -> Int
multiplicacao a b = a * b

multiplicacaoList:: [Int] -> Int
multiplicacaoList [] = 1
multiplicacaoList (a:as) = a * multiplicacaoList as

maior:: Int-> Int -> Int
maior a b | a > b = a
		  | otherwise = b

maiorList :: [Int] -> Int
maiorList [] = 0
maiorList (a:as) | a > (maiorList as) = a
				 | otherwise = (maiorList as)

menorDois:: Int-> Int -> Int
menorDois a b | a < b = a
		  	  | otherwise = b

menorTres :: Int-> Int-> Int -> Int
menorTres a b c | a < menorDois b c = a
		  	    | otherwise = menorDois b c

fat :: Int-> Int
fat 0 = 1
fat 1 = 1
fat 2 = 2
fat a | a > 2 = a * fat(a-1)

fibo :: Int -> Int
fibo 0 = 1
fibo 1 = 1
fibo a = (fibo (a-1)) + (fibo (a-2)) 

elemento :: [Int]-> Int -> Int
elemento [] b = 0
elemento (a:as) b | (b-1) < 0 = (a)
			   | otherwise = elemento (as) (b-1)

pertence :: [Int]-> Int -> Int
pertence [] b = 0
pertence (a:as) b | (a == b) = 1
			      | otherwise = pertence (as) (b)
