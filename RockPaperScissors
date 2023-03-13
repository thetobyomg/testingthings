
function getComputerChoice(){
    let i = Math.floor(Math.random() * 3);
    let outcome = i;

    if (i === 0) {
        outcome = "Rock";
    } else if (i === 1){
        outcome = "Paper";
    } else if(i === 2){
        outcome = "Scissors";
    } else{
        outcome = "Invalid";
    }
    return outcome;
}

function getPlayerChoice(){
    let playerInput = prompt("Please enter rock, paper, or scissors");
    return playerInput;
}

var playerScore = 0;
var compScore = 0;

function playRound(playerSelection, computerSelection) {
    let roundResult = "None.";
    let playSel = playerSelection.toUpperCase();
    let compSel = computerSelection.toUpperCase();

    if (playSel === "ROCK" && compSel === "SCISSORS" || playSel === "PAPER" && compSel === "ROCK" || playSel === "SCISSORS" && compSel === "PAPER"){
        playerScore += 1;
        roundResult = "Player wins!";

    } else if (playSel === "ROCK" && compSel === "PAPER" || playSel === "PAPER" && compSel === "SCISSORS" || playSel === "SCISSORS" && compSel === "ROCK"){
        compScore += 1;
        roundResult = "Computer wins!";

    } else if (playSel === compSel){
        roundResult = "Tie";
    } else {
        roundResult = "Invalid input!";
    }
    return roundResult;
}

function game(){
    for (let i = 0; i < 5; i++){
        let playerSelection = getPlayerChoice();
        let computerSelection = getComputerChoice();
        console.log('Player picked: ' + playerSelection);
        console.log('Computer picked: ' + computerSelection);
        console.log(playRound(playerSelection, computerSelection));
    }
}

function scoreResults(){
    let winner = "No one.";
    if (playerScore > compScore){
        winner = "Player wins!";
    } else if (compScore > playerScore){
        winner = "Computer wins!";
    } else {
        winner = "It's a tie!";
    }
    return winner;
}

game();
console.log("End results: " + scoreResults());
