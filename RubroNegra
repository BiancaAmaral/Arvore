from Tree import Tree

preto = True
vermelho = False

class RubroNegra:

    #construção do nó
    #inicialização dos objetos
    def __init__(self, item, chave, parente = None, esquerda = None, direita = None):
        self.item = item
        self.chave = chave
        self.parente = parente
        self.esquerda = esquerda
        self.direita = direita
        self.cor = vermelho

    ## Representação do nó como ums string.
    def __str__(self):

        if self.cor == preto:
            return str(self.item) + '\tpreto'
        else:
            return str(self.item) + '\tvermelho'

    ## retorna o avo do nó
    def avo(self):
        if self.parente != None:
            return self.parente.parente
        return None

    def tio(self):

        if self.avo() != None:
            if self.avo().esquerda == self.parente:
                return self.avo().direta
            elif self.avo().direita == self.parente:
                return self.avo().esquerda
            return None

    def reColorir(self):
        if self.cor == vermelho:
            self.cor = preto
        else:
            self.cor = vermelho

    def rotacaoDireita(self):

        self.parente.direita = self.esquerda

        if self.esquerda is not None:
            self.esquerda.parente = self.parente

        self.esquerda = self.parente
        self.parente = self.esquerda.parente
        self.esquerda.parente = self

        return self

    def rotacaoEsquerda(self):

        self.parente.esquerda = self.direta

        if self.direita is not None:
            self.direta.parente = self.parente

        self.direita  = self.parente
        if self.direita is not None:
            self.parente = self.direita.parente

        else:
            self.parente = None
        self.direita.parente = self

        return self
        
