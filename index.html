<!doctype html>
<html class="no-js" lang="en">
<head>
		<title>EmpCard</title>
		<meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
</head>
<body>
    <div class="content cardtester">
		<br />
		<p class="enemy_health">Enemy: <span>100</span></p>
		<span class="enemy_dmg"></span>
		<div class="enemy_deck"><span class="cv"></span><span class="h"></span><span class="w">WIN</span></div>
		<!-- -->
		<br />
		<p class="player_health">Player: <span>100</span></p>
		<span class="player_dmg"></span>
		<div class="player_deck"><span class="cv"></span><span class="h"></span><span class="w">WIN</span></div>
		<br />
		<div class="infoboard">
			<div class="game_msg"></div>
			<button type="button" id="contine">Start</button>
		</div>
	</div>
<script>
	var deck = [];
	var suit_numbers = [
		'','spades', 'hearts',
		'diamonds','clubs',
	];
	var player_health = 100;
	var player_card_value = 0;
	var enemy_health = 100;
	var enemy_card_value = 0;
	var next_player = 'e';
	var round_completed = false;
	var game_over = false;
	var game_started = false;
	//
	// var next_turn_index_array = [];
	// next_turn_index_array['p'] = 'h';
	// next_turn_index_array['h'] = 'p';
	//
	$(document).ready(function() {
		// reset_deck();
		//
		/*$('button#runtest').click(function() {
			test_add_card();
		});*/
		/*$('button#empgame').click(function() {
			reset_game();
			//
			game_redraw_health();
			game_start_round();
		});*/
		$('button#contine').click(function() {
			if (game_started==false) {
				game_started = true;
				$(this).html('Continue');
				reset_game();
				game_redraw_health();
				game_start_round();
			} else if (round_completed==false) {
				// if player has just finished their then prompt enemy to select their cards.
				if (next_player=='h') {
					game_enemy_turn2();
				}
				game_perform_battle();
				game_redraw_health();
				//
				$(this).html('End Round');
				round_completed = true;
				// immediately resolve battle and change button text to 'End Round'.
				// fade out the selected cards on the deck of the player who lost? might look rubbish
				// next_player = next_turn_index_array[next_player]; // toggle player/enemy turn
				if (next_player=='h') next_player = 'e';
				else next_player = 'h';
			} else if (round_completed && game_over) {
				game_clear_dmg_indicators();
				$(this).html('Continue');
				reset_game();
				game_redraw_health();
				game_start_round();
			} else if (round_completed && ( player_health <= 0 || enemy_health <= 0 )) {
				game_clear_dmg_indicators();
				perform_game_over();
				$(this).html('Restart');
			} else {
				game_clear_dmg_indicators();
				round_completed = false;
				$(this).html('Continue');
				$('div.game_msg').html('');
				game_start_round();
			}
		});
		/*var card_data = get_random_card();
		//
		if (card_data==false) {
			console.log('Attempt failed');
		} else {
			// console.log( 'Card: ' + card_data[0] + ' ' + card_data[1] );
			console.log( 'Card: ' + suit_numbers[card_data[0]] + ' c' + card_data[1] );
			$('div.cardtester').append('<div class="card ' + suit_numbers[card_data[0]] + ' c' + card_data[1] + '"></div>');
		}*/
	});
	function reset_game() {
		// reset_deck();
		player_health = 100;
		enemy_health = 100;
		// player_card_value = 0;
		// enemy_card_value = 0;
		// next_player = 'e'; /////////////
		//
		round_completed = false;
		game_over = false;
		$('div.game_msg').html('');
	}
	function perform_game_over() {
		game_over = true;
		if (player_health <= 0) $('div.game_msg').html('Player was defeated!');
		else if (enemy_health <= 0) $('div.game_msg').html('Enemy was defeated!');
	}
	function game_perform_battle() {
		if (player_card_value > enemy_card_value) {
			enemy_health = enemy_health - player_card_value;
			$('div.game_msg').html('Player Victory, ' + player_card_value + ' dmg!');
			$('div.player_deck > span.w').show();
			$('span.enemy_dmg').html('-' + player_card_value);
		} else if (player_card_value < enemy_card_value) {
			player_health = player_health - enemy_card_value;
			$('div.game_msg').html('Enemy Victory, ' + enemy_card_value + ' dmg!');
			$('div.enemy_deck > span.w').show();
			$('span.player_dmg').html('-' + enemy_card_value);
		} else {
			// it's a draw! //
			$('div.game_msg').html('Draw!');
		}
	}
	function game_redraw_health() {
		// $('div.player_deck span.h').html('Health: ' + player_health);
		$('p.player_health').html('Player: <span>' + player_health + '</span>');
		// $('div.enemy_deck span.h').html('Health: ' + enemy_health);
		$('p.enemy_health').html('Enemy: <span>' + enemy_health + '</span>');
	}
	function game_clear_dmg_indicators() {
		$('span.player_dmg').html('');
		$('span.enemy_dmg').html('');
	}
	function game_start_round() {
		reset_deck(); // ??
		player_card_value = 0;
		enemy_card_value = 0;
		$('div.enemy_deck .card').remove(); // clear decks
		$('div.player_deck .card').remove();
		$('div.enemy_deck > span.cv').html(''); // clear attack values
		$('div.player_deck > span.cv').html('');
		$('div.cardtester span.w').hide();
		for (var a = 1; a <= 5; a++) {
			var e_card = get_random_card();
			if (e_card==false) {}
			else $('div.enemy_deck').append(
				'<div data-val="' + e_card[1] + '" data-suit="' + e_card[0] + '" class="card ' + suit_numbers[e_card[0]] + ' c' + e_card[1] + ' cardback"></div>');
			var p_card = get_random_card();
			if (p_card==false) {}
			else $('div.player_deck').append(
				'<div data-val="' + p_card[1] + '" data-suit="' + p_card[0] + '" class="card ' + suit_numbers[p_card[0]] + ' c' + p_card[1] + '"></div>');
		}
		//
		if (next_player=='e') {
			game_enemy_turn2();
		}
		$('div.player_deck .card').click(function() { // is this being duplicated??
			player_deck_click(this);
		});
	}
	function game_enemy_turn() {
		var best_card = null;
		var card_values = [];
		$('div.enemy_deck .card').each(function() { // simple highest value check
			if (!best_card) best_card = this;
			if (parseInt($(this).attr('data-val')) > parseInt($(best_card).attr('data-val'))) best_card = this;
			card_values.push(parseInt($(this).attr('data-val'))); // used for pair matching
		});
		var this_number = 0;
		var best_pair_value = -1;
		$('div.enemy_deck .card').each(function() { // pairs value check
			for (var cv = 0; cv < card_values.length; cv++) {
				if (cv != this_number && parseInt($(this).attr('data-val'))==card_values[cv]) {
					// found a pair
					if (card_values[cv] * 2 >= parseInt($(best_card).attr('data-val'))) {
						best_pair_value = card_values[cv];
					}
				}
			}
			this_number++;
		});
		// /////////////// could be for each unique type of value we could grab all similar (could be up to 4) and total them up..
		// console.log(best_card);
		if (best_pair_value > -1) {
			$('div.enemy_deck .card.c' + best_pair_value).removeClass('cardback').addClass('selected');
			enemy_card_value = best_pair_value * 2;
		} else {
			$(best_card).removeClass('cardback').addClass('selected');
			enemy_card_value = parseInt($(best_card).attr('data-val'));
		}
		$('div.enemy_deck > span.cv').html(enemy_card_value);
		// next_player = 'p';
	}
	function game_enemy_turn2() {
		var strategies = [];
		$('div.enemy_deck .card').each(function() { // simple highest value check
			//
			var this_card_value = parseInt($(this).attr('data-val'));
			var strat_found = false;
			if (strategies.length) {
				for (var i = 0; i < strategies.length; i++) { // try to match it to a strategy
					if (strategies[i].card_value==this_card_value) { // one of possibly many mathcing methods??
						strat_found = true;
						// add to this strategy..
						strategies[i].strat_value = strategies[i].strat_value + this_card_value;
						strategies[i].card_list.push(this_card_value);
					}
				}
			}
			if (strat_found==false) { // otherwise make it it's own strategy
				var strat_id = strategies.length;
				strategies[strat_id] = [];
				strategies[strat_id]['card_value'] = this_card_value; // identifier
				strategies[strat_id]['strat_value'] = parseInt(strategies[strat_id]['card_value']); // total
				strategies[strat_id]['card_list'] = [ strategies[strat_id]['card_value'] ];
			}
		});
		//
		function strat_compare(a, b) {
            if (a.strat_value > b.strat_value) return -1;
            if (a.strat_value < b.strat_value) return 1;
            return 0;
        }
        strategies.sort(strat_compare); // sorted by strongest
		//
		$('div.enemy_deck .card.c' + strategies[0].card_value).removeClass('cardback').addClass('selected');
		enemy_card_value = strategies[0].strat_value;
		//
		$('div.enemy_deck > span.cv').html(enemy_card_value);
	}
	function player_deck_click(this_card) {
		if ($(this_card).hasClass('selected')) {
			$(this_card).removeClass('selected');
			player_card_value = player_card_value - parseInt($(this_card).attr('data-val'));
		} else {
			var can_add = false;
			// perform check
			if (player_card_value > 0) { // they must have something already selected
				$('div.player_deck .card').each(function() {
					if ($(this).hasClass('selected') && parseInt($(this).attr('data-val'))==parseInt($(this_card).attr('data-val')) ) {
						can_add = true;
					}
				});
			} else can_add = true;
			//
			if (can_add) {
				$(this_card).addClass('selected');
				player_card_value = player_card_value + parseInt($(this_card).attr('data-val'));
			}
		}
		$('div.player_deck > span.cv').html(player_card_value);
	}
	function reset_deck() {
		for (var s = 1; s <= 4; s++) { //suit
			deck[s] = [];
			for (var c = 2; c <= 14; c++) { //card
				deck[s][c] = false; // not taken
			}
		}
	}
	function getRandomInt(min, max) {
		min = Math.ceil(min);
		max = Math.floor(max);
		return Math.floor(Math.random() * (max - min)) + min; //The maximum is exclusive and the minimum is inclusive
	}
	function get_random_card() {
		var found = false;
		var attempts = 0;
		while (found==false && attempts < 50) {
			var suit = getRandomInt(1, 5);
			var val = getRandomInt(2, 15);
			if (deck[suit][val]==false) {
				found = true;
				deck[suit][val] = true; // mark as taken
				return [ suit, val ];
			}
			attempts++;
		}
		return false;
	}
</script>
<style>
	html {
		font-family: arial;
		font-size: 14.4px;
		background-color: #ebebeb;
	}
	div.card {
		background-color: #fefefe;
		/*border: 1px solid #ddd;*/
		border: 1px solid #999;
		border-radius: 1px;
		/*height: 22px;*/
		height: 40px;
		/*width: 20px;*/
		width: 26px;
		display: inline-block;
		/*padding: 2px;*/
		text-align: center;
		padding-top: 10px;
		-webkit-box-sizing: border-box;
		-moz-box-sizing: border-box;
		box-sizing: border-box;
	}
	div.card.hearts, div.card.diamonds { /* colour them red */
		color: #e00;
	}
	div.card.spades:before { content: "\2660"; }
	div.card.clubs:before { content: "\2663"; }
	div.card.hearts:before { content: "\2665"; }
	div.card.diamonds:before { content: "\2666"; }
	div.card.c2:after { content: "2"; }
	div.card.c3:after { content: "3"; }
	div.card.c4:after { content: "4"; }
	div.card.c5:after { content: "5"; }
	div.card.c6:after { content: "6"; }
	div.card.c7:after { content: "7"; }
	div.card.c8:after { content: "8"; }
	div.card.c9:after { content: "9"; }
	div.card.c10:after { content: "10"; }
	div.card.c11:after { content: "J"; }
	div.card.c12:after { content: "Q"; }
	div.card.c13:after { content: "K"; }
	div.card.c14:after { content: "A"; }

	div.card.cardback:after { content: "\00A0"; }
	div.card.cardback:before { content: "\00A0"; }

	div.enemy_deck, div.player_deck {
		border: 1px solid #555;
		border-radius: 2px;
		width: 200px;
		height: 50px;
		display: block;
		background-color: #bbb;
		position: relative;
	}
	div.enemy_deck span.h, div.player_deck span.h {
		position: absolute;
	    /*right: -28px;*/
	    right: -78px;
	    top: 6px;
	    text-align: left;
    	width: 74px;
	}
	div.enemy_deck span.cv, div.player_deck span.cv {
		position: absolute;
	    /*right: -64px;*/
	    /*top: 28px;*/
	    right: -66px;
    	top: 16px;
	    text-align: left;
    	width: 60px;
	}
	div.enemy_deck > .card, div.player_deck > .card {
		margin-top: 4px;
		margin-left: 4px;
	}
	div.player_deck > .card.selected {
		top: -8px;
    	position: relative;
	}
	div.player_deck > .card {
		cursor: pointer;
	}
	div.enemy_deck > .card.selected {
		top: 8px;
    	position: relative;
	}
	div.infoboard {
		width: 200px;
		text-align: center;
	}
	div.game_msg {
		/*width: 200px;*/
		width: 100%;
		height: 24px;
		background-color: #ccc;
		margin-bottom: 10px;
		padding: 5px;
		text-align: left;
	}
	div.enemy_deck span.w, div.player_deck span.w {
		position: absolute;
	    right: -60px; /* -120px; */
    	top: 16px;
    	font-weight: bold;
    	color: cornflowerblue;
    	display: none;
	}
	button {
		border-style: none;
	    width: 120px;
	    height: 42px;
	    border: 1px solid #333;
	    cursor: pointer;
	    background-color: beige;
	}
	button:hover {
		background-color: #f5f570;
	}
	p.enemy_health, p.player_health {
		margin: 0;
    	margin-bottom: 4px;
    	display: inline-block;
    	color: #444;
	}
	p.enemy_health > span, p.player_health > span {
		color: #000;
	}
	span.enemy_dmg, span.player_dmg {
		color: #f00;
		font-weight: bold;
	}
</style>

<!-- http://localhost:8085/pages/emp.php -->
</body>
</html>