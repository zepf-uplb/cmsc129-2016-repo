<CODE> := simula<LINE>tapos
<LINE> := <STMT><LINE> | <STMT>
<STMT> := <OUT> | <IN> | <ARITH> | <BOOL_A> | <VARDEC_A> | <ASS> | <FILE> | <FXN> | <RETURN> | <FXNCALL_A> | <WHILE> | <FOR> | <COND> | ε
<OUT> := isulat(<ACTION>); | isulat(<STRING>);
<IN> := ikuha(<VAR>);
<BIN_A> := (<ACTION>,<ACTION>)
<BIN_B> := (<BOOL_B>,<BOOL_B>)
<ARITH_A> := ( plas | maynus | dibayd | multiplay | modyulo )<BIN_A>; 
<ARITH_B> := ( plas | maynus | dibayd | multiplay | modyulo )<BIN_A>
<BOOL_A> := ( at | o )<BIN_B>; | hinde(<BOOL_B>); | ( masmalaki | masmaliit | parehas | hindeRehas |lakiRehas | liitRehas )<BIN_A>;
<BOOL_B> := ( at | o )<BIN_B>; | hinde(<BOOL_B>); | ( masmalaki | masmaliit | parehas | hindeRehas |lakiRehas | liitRehas )<BIN_A>
<VARDEC_A> := <TYPE><VARDEC_B>;
<VARDEC_B> := <INIT> | <INIT>,<VARDEC_B>
<INIT> := <VAR> | <VAR>=<ACTION>
<TYPE> := numero | karakter | lutang
<ASS> := <VAR>=<ACTION>;
<FILE> := payl(<ACTION>); | payl(<STRING>);
<FILE_OUT> := isulatSaPayl(<ACTION>); | isulatSaPayl(<STRING>);
<FILE_IN> := ikuhaSaPayl(<VAR>);
<FXN> := panksyon<TYPE><FXNNAME>(<PARAM>):<LINE>noysknap;
<RETURN> := ibigay(<ACTION>); | ibigay();
<PARAM> := <TYPE><VAR> | <TYPE><VAR>,<PARAM> | ε
<FXNCALL_A> := $<FXNNAME>(<FCPARAM_A>);
<FXNCALL_B> := $<FXNNAME>(<FCPARAM_A>)
<FCPARAM_A> := <ACTION><FCPARAM_B> | ε
<FCPARAM_B> := ,<ACTION><FCPARAM_B> | ε 
<WHILE> := habang(<BOOL_B>):<LINE>gnabah;
<FOR> := por(<INIT>;<BOOL_B>;<INIT>):<LINE>rop;
<COND> := kung(<BOOL_B>):<LINE>gnuk;<ELSIF><ELSE>
<ELSIF> := eKung(<BOOL_B>):<LINE>gnuKe;<ELSIF> | ε
<ELSE> := kungHinde:<LINE>edniHgnuk; | ε
<RANDOM> := random(<ACTION>)
<SQRT> := parigat(<ACTION>)
<ACTION> := <FXNCALL_B> | <ARITH_B> | <VAR> | <NUMBER> | <RANDOM> | <SQRT>
<VAR> := <ALPHABET> | <ALPHABET><ARR>
<ARR> := [<ACTION>]<ARR> | [<ACTION>]
<FXNNAME> := <ALPHABET>
<STRING> := “<ANY>”
<FILE_OUT> := isulatSaPayl(<ACTION>); | isulatSaPayl(<STRING>);
<FILE_IN> := ikuhaSaPayl(<VAR>);