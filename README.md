# Calculadora-de-partidas-ranqueadas
Este projeto calcula o nível de vitórias e derrotas de um jogador e relaciona o resultado com o nível proporcional.


let saldoVitoria = calcularPartidas(50, 10)
let nivel = calcularNivel(saldoVitoria)

console.log(`O Herói tem de saldo de ${saldoVitoria} e está no nível de ${nivel}`)

function calcularPartidas(vitoria, derrota){
    let resultado = vitoria - derrota
    return resultado
}

function calcularNivel(saldo){
    let nivelHeroi;
    switch(true){
        case saldo <= 10:
            nivelHeroi = "Ferro"
            break
        
        case saldo >= 11 && saldo <= 20:
            nivelHeroi = "Bronze"
            break

        case saldo >= 21 && saldo <= 50:
            nivelHeroi = "Prata"
            break

        case saldo >= 51 && saldo <= 80:
            nivelHeroi = "Ouro"
            break

        case saldo >= 81 && saldo <= 90:
            nivelHeroi = "Diamante"
            break

        case saldo >= 91 && saldo <= 100:
            nivelHeroi = "Lendário"
            break

        case saldo >= 101:
            nivelHeroi = "Imortal"
            break
    }
    return nivelHeroi
}
