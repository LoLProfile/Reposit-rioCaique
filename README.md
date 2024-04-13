# RepositórioCaique
programa {
  funcao inicio() {
    cadeia cupom, resposta
    real consumo_hamburguer1, consumo_cheeseburguer1, consumo_fritas1, consumo_refri1, consumo_milkshake1, consumo_hamburguer2, consumo_cheeseburguer2, consumo_fritas2, consumo_refri2, consumo_milkshake2, valor_total1, valor_total2, valor_apos_desconto1, valor_apos_desconto2
    escreva("Quantos hambúrgueres você consumiu?\n")
    leia(consumo_hamburguer1)
    escreva("Quantos cheeseburguers você consumiu?\n")
    leia(consumo_cheeseburguer1)
    escreva("Quantas fritas você consumiu?\n")
    leia(consumo_fritas1)
    escreva("Quantos refrigerantes você consumiu?\n")
    leia(consumo_refri1)
    escreva("Quantos milkshakes você consumiu?\n")
    leia(consumo_milkshake1)
    limpa()
    valor_total1=consumo_hamburguer1*12+consumo_cheeseburguer1*15+consumo_fritas1*8+consumo_refri1*5+consumo_milkshake1*9.50
    escreva("Você possui algum cupom?\n")
    leia(cupom)
    limpa()
    se (cupom=="Sim"){
      valor_apos_desconto1=valor_total1*0.9
      enquanto (valor_apos_desconto1<=100){
        escreva("Você gostaria de adicionar algo a mais?\n")
        leia(resposta)
        limpa()
        se (resposta=="Sim"){
         escreva("Quantos hambúrgueres você quer a mais?\n")
         leia(consumo_hamburguer2)
         escreva("Quantos cheeseburguers você quer a mais?\n")
         leia(consumo_cheeseburguer2)
         escreva("Quantas fritas você quer a mais?\n")
         leia(consumo_fritas2)
         escreva("Quantos refrigerantes você quer a mais?\n")
         leia(consumo_refri2)
         escreva("Quantos milkshakes você quer a mais?\n")
         leia(consumo_milkshake2)
         limpa()
         valor_total2=(consumo_hamburguer2*12+consumo_cheeseburguer2*15+consumo_fritas2*8+consumo_refri2*5+consumo_milkshake2*9.50)+valor_total1
         valor_apos_desconto2=valor_total2*0.9
         escreva("O valor do seu pedido é:\n", valor_apos_desconto2, " R$")
         pare
        }
        se (resposta=="Não"){
          escreva("O valor do seu pedido é:\n", valor_apos_desconto1, " R$")
          pare
        }
      }
      enquanto (valor_apos_desconto1>100){
        escreva("O valor do seu pedido é:\n", valor_apos_desconto1, " R$")
        pare
      }
    }
    se (cupom=="Não"){
      escolha (valor_total1){
        caso 1:
        escreva("O valor do seu pedido é de:\n", valor_total1, " R$")
        pare
        caso contrario:
        escreva("O valor do seu pedido é de:\n", valor_total1, " R$")
        pare
      }
    }
  }
}
