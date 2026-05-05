Sistema de Gestão de Notas - Projeto

- O usuário insere as notas uma a uma.

- **Cadastro das notas**
    - As notas válidas (entre 0 e 10) são armazenadas em uma **lista**.
    - O usuário digita -`1` quando quiser parar de inserir as notas.

- **Cálculo da média**
    - Soma todas as notas da lista.
    - Divide pela quantidade de notas para obter a média.

- **Determinação da situação**
    - Se a média for **maior ou igual a 7**, o aluno está **Aprovado**.
    - Se a média for **menor que 7**, o aluno está **Reprovado**.

- **Exibição do relatório final**
    - Mostra todas as notas digitadas.
    - Exibe a média calculada (com duas casas decimais).
    - Mostra a situação do aluno (Aprovado/Reprovado).
    
    ```python
    Função para cadastrar notas
    ```
    
    ```python
    def cadastrar_notas():
    notas = []
    while True:
    try:
    nota = float(input("Digite a nota do aluno (ou -1 para encerrar): "))
    if nota == -1:  # condição de parada
    break
    if 0 <= nota <= 10:  # validação da nota
    notas.append(nota)
    else:
    print("⚠️ A nota deve estar entre 0 e 10.")
    except ValueError:
    print("⚠️ Digite um valor numérico válido.")
    return notas
    ```
    
    ```python
    Função para calcular média
    ```
    
    ```python
    def calcular_media(notas):
    if len(notas) == 0:
    return 0
    return sum(notas) / len(notas)
    ```
    
    ```python
    Função para determinar situação
    ```
    
    ```python
    def verificar_situacao(media):
    if media >= 7:
    return "Aprovado ✅"
    else:
    return "Reprovado ❌"
    ```
    
    ```python
    Função para exibir relatório
    ```
    
    ```python
    def exibir_relatorio(notas, media, situacao):
    print("\n===== RELATÓRIO FINAL =====")
    print(f"Notas inseridas: {notas}")
    print(f"Média: {media:.2f}")
    print(f"Situação: {situacao}")
    ```
    
    ```python
    Programa principal
    ```
    
    ```python
    def main():
    print("=== Sistema de Gestão de Notas ===")
    notas = cadastrar_notas()
    media = calcular_media(notas)
    situacao = verificar_situacao(media)
    exibir_relatorio(notas, media, situacao)
    ```
    
    ```python
    Executa o programa
    ```
    
    ```python
    if **name** == "**main**":
    main()
    ```
    


