function sqmode(varname, value)
	avi_swtch = ipc.readLvar("AvionicsElecPower")	
	
		if avi_swtch==1 and (value==4 or value==3) then
			--squawk mode charlie
			ipc.writeSB(0x7B91, 0)
		else
			--squawk mode stand by
			ipc.writeSB(0x7B91, 1)
		end
	--else
		--squawk mode stand by
		--ipc.writeSB(0x7B91, 1)
	--end
end

function sqident(varname, value)
	if value==1 then
	--squawk ident
		ipc.writeSB(0x7b93, 1)
	end
end

event.Lvar("L:xpdr_onoff_knob_pos", 500,"sqmode")
event.Lvar("L:xpdr_ident_button", 500,"sqident")
