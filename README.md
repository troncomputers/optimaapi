## Błędy prosimy zgłaszać na zakładce `Issues`

# CHANGELOG
1. Przejście na EF Core dla przyszłego rozwoju oprogramowania. Prostsze mapowanie chorych nazw kolumn.
2. Endpoint api/bankaccounts przeniesiony do api/bank/accounts. Celem jest starać się utrzymać jeden kontroler na konkretny moduł Optimy
3. Lista definicji dokumentów api/documents/definitions
4. Zmiana w wymaganiach pól. Pola typu string z flagą `AllowEmpty` nie są już wymagane i będą miały domyślną wartość jako pusty string.
5. Pola innego typu (non nullable) np. short, decimal, int będą również przyjmowały domyślną wartość. Najczęściej 0. Pola typu DateTime będą domyślnie przyjmowały wartość Now/Today
6. Dla pól typów opisanych w punktach wyżej - jeśli domyślna wartość będzie inna niż string.empty lub 0 itp, to będzie w dokumentacji opisana jaka jest wartość domyślna
7. Błędy krytyczne (nieobsłużone przez nas) będą zwracały status 500, w przypadku innych błędów (niepoprawnych danych w body) będzie zwracane 400 (Bad Request) z treścią błędu. Głównie tyczy się to endpointów typu POST.
