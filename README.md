# Scrum
class Scrum:
    def __init__(self):
        self.necessidades = []
        self.sprints = []

    def adicionar_necessidade(self, necessidade):
        self.necessidades.append(necessidade)

    def priorizar_necessidades(self):
        # Implemente a lógica de priorização aqui
        return self.necessidades

    def criar_sprint(self, necessidades):
        sprint = Sprint(necessidades)
        self.sprints.append(sprint)
        return sprint

    def executar_sprint(self, sprint):
        # Implemente a lógica de execução do sprint aqui
        print("Executando sprint...")

class Sprint:
    def __init__(self, necessidades):
        self.necessidades = necessidades
        self.tarefas = []

    def adicionar_tarefa(self, tarefa):
        self.tarefas.append(tarefa)

    def executar_tarefa(self, tarefa):
        # Implemente a lógica de execução da tarefa aqui
        print("Executando tarefa...")

# Creat um objeto Scrum
scrum = Scrum()

# Adicione necessidades
scrum.adicionar_necessidade("Desenvolver um aplicativo móvel")
scrum.adicionar_necessidade("Criar um site de e-commerce")

# Priorize necessidades
necessidades_priorizadas = scrum.prioriar_necessidades()

# Creat um sprint
sprint = scrum.criar_sprint(necessidades_priorizadas)

# Execute o sprint
scrum.executar_sprint(sprint)
