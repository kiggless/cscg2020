# Pseudocode

Perl script does random stuff

```python
INPUT = "@~^UgAAAA==v,Zj;MPKtb/|r/|Y4+|0sCT{XKN@#@&H/T$G6,J;?/M,P_qj{g6K|I3)d{sJ)VTE~,#~rF}x^X~,JgGwJexkAAA==^#~@"

for part in INPUT.split('-'):
    q = 0
    for p in part.split():
        p = p.replace("\|", ":.:")
        p = p.replace(":", "..")
        Q = len(p) if p else p
        q += Q if q else Q * 20

print()

x = ""
y = """
#@~^UgAAAA==v,Zj;MPKtb/|r/|Y4+|0sCT{XKN@#@&H/T$G6,J;?/M,P_qj{g6K|I3)d{sJ)VTE~,#~rF}x^X~,JgGwJexkAAA==^#~@
''"""

x += y[21]
x += y[25]
x += y[28]
x += " "
x += chr(0xa * 0x1c - 0xB0)
print(x + "arder")
```

polyrun => can be run in multiple ways?

suspicious `'';` at the start of lines

suspicious comment: `#@~^UgAAAA==v,Zj;MPKtb/|r/|Y4+|0sCT{XKN@#@&H/T$G6,J;?/M,P_qj{g6K|I3)d{sJ)VTE~,#~rF}x^X~,JgGwJexkAAA==^#~@`

looks like it is enclosed by `#@~` `#~@` or something like that

Searching for `#@~` on Google brings up something about VisualBasic Script decryption.
Searching further, it looks like this is some kind of encrypted VBS code.
`'` is a comment in VBS, so most of the perl code is commented out.
Searching further this seems to be encrypted with `JScript.Encode`.
Decoder at <https://gist.github.com/bcse/1834878>.

```
'';open(Q,$0);while(<Q>){if(/^#(.*)$/){for(split('-',$1)){$q=0;for(split){s/\|/:.:/xg;s/:/../g;$Q=$_?length:$_;$q+=$q?$Q:$Q*20;};}}}print"\n";
'';$?=
' CSCG{This_is_the_flag_yo}
MsgBox "CSCG[THIS_NOT_REAL_FLAG]", VBOKOnly, "Nope"
eval eval '"'."'"."'".';'.'\\'.'$'.'_'.('{'^'[').'='.('{'^'[').'\\'.'"'.'\\'.'"'.';'.('!'^'+')."'"."'".';'.('\\').'$'.'_'.'_'.('{'^'[').'='.('{'^'[').'\\'.'"'.('!'^'+').'#'.'\\'.'@'.'~'.'^'.('{'^'.').('`'|"'").('`'^'!').('`'^'!').('`'^'!').('`'^'!').'='.'='.('['^'-').','.('{'^'!').('`'|'*').';'.('`'^'-').('{'^'+').('`'^'+').('['^'/').('`'|'"').'/'.'|'.('['^')').'/'.'|'.('{'^'"').('^'^('`'|'*')).'+'.'|'.(('^')^('`'|'.')).('['^'(').('`'^'#').('{'^'/').'\\'.'{'.('{'^'#').('`'^'+').('`'^'.').'\\'.'@'.'#'.'\\'.'@'.'&'.('`'^'(').'/'.('{'^'/').'\\'.'$'.('`'^"'").('^'^('`'|'(')).','.('`'^'*').';'.'?'.'/'.('`'^'-').','.('{'^'+').'_'.('['^'*').('`'|'*').'\\'.'{'.('`'|"'").('^'^('`'|'(')).('`'^'+').'|'.('`'^(')')).('^'^('`'|'-')).')'.('`'|'$').'\\'.'{'.('['^'(').('`'^'*').')'.('{'^'-').('{'^'/').('`'^'%').'~'.','.'#'.'~'.('['^')').('`'^'&').'\\'.'}'.('['^'#').'^'.('{'^'#').'~'.','.('`'^'*').('`'|"'").('`'^"'").('['^',').('!'^'^').('`'^'*').('`'|'%').('['^'#').('`'|'+').('`'^'!').('`'^'!').('`'^'!').'='.'='.'^'.'#'.'~'.'\\'.'@'.('!'^'+')."'"."'".'\\'.'"'.';'.('!'^'+')."'"."'".';'.('`'|'&').('`'|'/').('['^')').('{'^'[').'('.('`'|'-').('['^'"').('{'^'[').'\\'.'$'.('`'|'/').('`'|'/').('^'^('`'|'/')).('`'|'/').('`'^')').'='.('^'^('`'|'.')).';'.('{'^'[').'\\'.'$'.('`'|'/').('`'|'/').('^'^('`'|'/')).('`'|'/').('`'^')').('{'^'[').'<'.'='.('{'^'[').('^'^('`'|'/')).';'.('{'^'[').'\\'.'$'.('`'|'/').('`'|'/').('^'^('`'|'/')).('`'|'/').('`'^')').'+'.'+'.')'.('{'^'[').'\\'.'{'.('`'|')').('`'|'&').'('.'\\'.'$'.('`'|'/').('`'|'/').('^'^('`'|'/')).('`'|'/').('`'^')').('{'^'[').'='.'='.('{'^'[').('^'^('`'|'.')).')'.'\\'.'{'.'\\'.'$'.'_'.'.'.'='.('['^'(').('['^'.').('`'|'"').('['^'(').('['^'/').('['^')')."\(".'\\'.'$'.'_'.'_'.','.('^'^('`'|',')).('^'^('`'|'/')).'+'.'\\'.'$'.('`'|'/').('`'|'/').('^'^('`'|('/'))).('`'|'/').('`'^')').','.('^'^('`'|'/')).')'.';'.'\\'.'$'.'_'.'.'.'='.('['^'(').('['^'.').('`'|"\"").('['^'(').('['^'/').('['^')').'('.'\\'.'$'.'_'.'_'.','.('^'^('`'|',')).('^'^('`'|'+')).'+'.'\\'.'$'.('`'|'/').('`'|'/').('^'^('`'|'/')).('`'|'/').('`'^')').','.('^'^('`'|'/')).')'.';'.'\\'.'$'.'_'.'.'.'='.('['^'(').('['^'.').('`'|'"').('['^'(').('['^'/').('['^')').'('.'\\'.'$'.'_'.'_'.','.('^'^("\`"|',')).(':'&'=').'+'.'\\'.'$'.('`'|'/').('`'|'/').('^'^('`'|'/')).('`'|'/').('`'^')').','.('^'^("\`"|'/')).')'.';'.'\\'.'$'.'_'.'.'.'='.'\\'.'"'.('{'^'[').'\\'.'"'.';'.'\\'.'}'.('`'|'%').('`'|',').('['^'(').('`'|'%').'\\'.'{'.('{'^'[').'\\'.'$'.'_'.('{'^'[').'.'.'='.('{'^'[').('`'|'#').('`'|'(').('['^')').'('.('^'^('`'|'.')).('['^'#').('`'|'!').'*'.('^'^('`'|'.')).('['^'#').('^'^('`'|'/')).('`'|'#').'-'.('^'^('`'|'.')).('['^'#').('`'^'"').('^'^('`'|'.')).')'.';'.'\\'.'}'.'\\'.'}'.('!'^'+').("'")."'".';'.('{'^'[').('['^'+').('['^')').('`'|')').('`'|'.').('['^'/').('{'^'[').'\\'.'$'.'_'.('{'^'[').'.'.('{'^'[').'\\'.'"'.('`'|'!').('['^')').('`'|'$').('`'|'%').('['^')').'\\'.'"'.';'.'"';$:=('.');
```

Probably opens a message box with `CSCG[THIS_NOT_REAL_FLAG]` if run somehow,
but the real flag is in the decrypted comment.

Flag: `CSCG{This_is_the_flag_yo}`
