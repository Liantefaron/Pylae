roll(											[Humans from Master Library]
	dice(										dice(count, sides, modifier)
		1,8,									1d8 + ...
		if($st < 7,								mod: ST1-6: +51 [52-59" = 130-148 cm] OR
			51,
			if($st < 10,						mod: ST7-9: +54+3*(ST-7) [58-68" = 145-170 cm] OR
				54 + ($st - 7) * 3,
				if($st == 10,					mod: ST10: +62 [63-70" = 158-175 cm] OR
					62,
					if($st < 14,				mod: ST11-13: 64+3*(ST-11) [65-78" = 163-195 cm] OR
						64 + ($st - 11) * 3,
						73						mod: ST14+: +73 [74-81" = 185-203 cm]
					)
				)
			)
		)
	)
)

Size Modifiers:
-2	 80 - 100 cm
-1	110 - 150 cm (=~ ST1-7 results above)  [Arrodo: 110-130cm, 27-35kg (44-52", 54-70lb) / Taipuisa: 130-150cm, ±35kg (52-60", 65-75lb)]
0	160 - 200 cm (=~ ST8-14 results above) [Imisen: = Humans + 2 in & + 1lb ?]
1	210 - 300 cm [Cetosi: 250-300cm, 300-400kg (100-120", 600-800lb)]
2	310 - 500 cm


roll(											[Arrodo SM-1 (44-52" in set of 4", 54-70lb)]
	dice(										dice(count, sides, modifier)
		1,4,									1d4 + ...
		if($st < 7,								mod_frail: ST1-6: [38-41" = 97-104 cm] OR
			37,
			if($st < 10,						mod_weak: ST7-9: [41-45" = 104-115 cm] OR
				40 + ($st - 7),
				if($st == 10,					mod_avg: ST10: [45-49" = 115-125 cm] OR
					44,
					if($st < 14,				mod_strong: ST11-13: [47-52" = 120-133 cm] OR
						46 + ($st - 11),
						49						mod_heroic: ST14+: [50-53" = 128-135 cm]
					)
				)
			)
		)
	)
)
collapsed height formula: roll(dice(1,4,if($st < 7,37,if($st < 10,40 + ($st - 7),if($st == 10,44,if($st < 14,46 + ($st - 11),49))))))

roll(											[Taipuisa SM-1 Racial ST-1 (52-60" in sets of 4", 65-75lb)]
	dice(										dice(count, sides, modifier)
		1,4,									1d4 + ...
		if($st < 6,								mod_frail: ST1-5: [50-54" = 127-137 cm] OR
			49,
			if($st < 9,							mod_weak: ST6-8: [51-56" = 130-142 cm] OR
				50 + ($st - 6),
				if($st == 9,					mod_avg: ST9: [54-57" = 137-145 cm] OR
					53,
					if($st < 13,				mod_strong: ST10-12: [56-61" = 142-155 cm] OR
						55 + ($st - 10),
						57						mod_heroic: ST13+: [58-61" = 147-155 cm]
					)
				)
			)
		)
	)
)
collapsed height formula: roll(dice(1,4,if($st < 6,49,if($st < 9,50 + ($st - 6),if($st == 9,53,if($st < 13,55 + ($st - 10),57))))))

roll(											[Cetosi SM+1 Racial ST+4 (100-120" in sets of 8", 600-800lb)]
	dice(										dice(count, sides, modifier)
		1,8,									1d8 + ...
		if($st < 11,							mod_frail: ST1-10: [98-105" = 249-267 cm] OR
			97,
			if($st < 14,						mod_weak: ST11-13: [99-112" = 251-284 cm] OR
				101 + ($st - 12) * 3,
				if($st == 14,					mod_avg: ST14: [106-113" = 269-287 cm] OR
					105,
					if($st < 18,				mod_strong: ST15-17: [108-121" = 274-307 cm] OR
						107 + ($st - 15) * 3,
						114						mod_heroic: ST18+: [115-123" = 292-312 cm]
					)
				)
			)
		)
	)
)
collapsed height formula: roll(dice(1,8,if($st < 11,97,if($st < 14,101 + ($st - 12) * 3,if($st == 14,105,if($st < 18,107 + ($st - 15) * 3,114))))))

==================================================================

WEIGHT FORMULAS

												[Human from Master Library - only a tad overcomplicated]
roll(
	dice(1,										dice(count, sides, modifier): 1 die
		if($st < 11,								sides_normal: ST1-10
			61,											61 sides (1-61) OR
			if($st < 14,							sides_strong: ST11-13
				71 + ($st - 11) * 10,					71 sides (1-71) up to 91 (1-91) sides
				101									sides_heroic: ST14+ -> 101 (1-101) sides
			)
		),
		if($st < 7,									mod_frail: ST1-6
			60,											+60
			if($st < 10,							mod_weak: ST7-9
				75 + ($st - 7) * 15,					+75 up to +105
				if($st == 10, 						mod_avg: ST10
					115,								+115
					if($st < 14,					mod_strong: ST11-13
						125 + ($st - 11) * 15,			+125 up to +170
						170							mod_heroic: ST14+ -> +170
					)
				)
			)
		)
	)
)

												[Arrodo SM-1 54-70lb]
roll(
	dice(1,12,										dice(count, sides, modifier): 1d12
		if($st < 7,									mod_frail: ST1-6
			51,											+51 [52-64]
			if($st < 10,							mod_weak: ST7-9
				53,										+53 [54-66]
				if($st == 10, 						mod_avg: ST10
					55,									+55 [56-68]
					if($st < 14,					mod_strong: ST11-13
						58,								+58 [59-71]
						61							mod_heroic: ST14+ -> +61 [62-74]
					)
				)
			)
		)
	)
)
collapsed weight formula: roll(dice(1,12,if($st < 7,51,if($st < 10,53,if($st == 10,55,if($st < 14,58,61))))))

												[Taipuisa SM-1 ST-1 60-80lb]
roll(
	dice(1,8,										dice(count, sides, modifier): 1d8
		if($st < 6,									mod_frail: ST1-5
			57,											+57 [58-66]
			if($st < 9,								mod_weak: ST6-8
				61,										+61 [62-70]
				if($st == 9, 						mod_avg: ST9
					69,									+69 [70-78]
					if($st < 13,					mod_strong: ST10-12
						73,								+73 [74-82]
						75							mod_heroic: ST13+ -> +75 [76-84]
					)
				)
			)
		)
	)
)
collapsed weight formula: roll(dice(1,8,if($st < 6,57,if($st < 9,61,if($st == 9,69,if($st < 13,73,75))))))
												[Cetosi SM+1 ST+4 600-800lb]
roll(
	dice(1,60,										dice(count, sides, modifier): 1d60
		if($st < 11,									mod_frail: ST5-10
			51,											+579 [580-640]
			if($st < 14,							mod_weak: ST11-13
				53,										+619 [620-680]
				if($st == 14, 						mod_avg: ST14
					55,									+669 [670-730]
					if($st < 18,					mod_strong: ST15-17
						699,							+699 [700-760]
						749							mod_heroic: ST17+ -> +749 [750-810]
					)
				)
			)
		)
	)
)
collapsed weight formula: 
roll(dice(1,60,if($st < 11,51,if($st < 10,53,if($st == 14,55,if($st < 18,699,749))))))