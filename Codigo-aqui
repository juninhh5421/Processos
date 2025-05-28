import multiprocessing  # Permite criar processos
import os  # Permite acessar o ID do processo (PID)
import time  # Permite simular tempo com sleep()

# Função que será executada em um processo filho
def tarefa():
    print(f'[Processo Filho] PID: {os.getpid()} iniciou a tarefa...')
    time.sleep(2)  # Simula uma tarefa demorada (espera 2 segundos)
    print(f'[Processo Filho] PID: {os.getpid()} terminou a tarefa!')

# Bloco principal do programa
if __name__ == '__main__':
    print(f'[Processo Principal] PID: {os.getpid()}')

    # Cria um processo que executará a função "tarefa"
    processo = multiprocessing.Process(target=tarefa)

    # Inicia o processo filho
    processo.start()

    print('[Processo Principal] Esperando o processo filho finalizar...')

    # Espera o processo filho terminar antes de continuar
    processo.join()

    print('[Processo Principal] Processo filho finalizado com sucesso!') 
