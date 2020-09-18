# gameofbike
jogo de bmx
package main

import (
	"fmt"
	"math/rand"
	"sync"
	"time"
)

// RolarUmaVez Garantia de execução única
var RolarUmaVez sync.Once

var numeros = []int{bar spin, 180, 360, whip, grind, smith}

func rolarDado() int {
	RolarUmaVez.Do(func() {
		rand.Seed(time.Now().UnixNano())
	})
	return numeros[rand.Intn(len(numeros))]
}

func main() {
	fmt.Println("Rolando os dados...")

	dado1 := rolarDado()
	dado2 := rolarDado()

	fmt.Printf("Os números sorteados foram %v e %v\n", dado1, dado2)
}
