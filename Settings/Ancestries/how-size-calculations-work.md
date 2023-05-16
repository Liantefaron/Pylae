roll(											[Humans]
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
-1	110 - 150 cm (=~ ST1-7 results above)
0	160 - 200 cm (=~ ST8-14 results above)
1	210 - 300 cm
2	310 - 500 cm