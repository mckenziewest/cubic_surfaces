Below is the information about the magma code contained in 
the files 
	dP2H1.magma 
and 
	backgroundFunctions.magma
which can be found in this directory.
The code was developed by Mckenzie West as part of the Algebraic 
Geometry BOOTCAMP in Salt Lake City, Utah which began on 
July 6, 2015.  It is intended to compute the lines on as well as
the quotient of the Br X by Br Q, i.e.
H1(Gal(Qbar/Q),Pic(Xbar)), of a degree 2 del Pezzo 
surface, X, which is defined by some
	w^2 = f(x,y,z),
where f is any quartic polynomial over Q.
Send any comments or questions to 
mwest6 (at) emory (dot) edu

Cheers,
Mckenzie




INSTRUCTIONS: 
In order to use the code follow the steps listed here:
	1. Download the files into a single folder.
	2. In a terminal, cd into the folder that the files are located.
	3. Open magma.
	4. To load all functions listed at the end of this document,
		enter the following command into magma:
			load "dP2H1.magma";
	5. You have several choices on what you can compute.
		a.) To output the lines on X: w^2 = F(x,y,z), where F is 
			a quartic over Q, as well as their mutual field of 	
			definition,  use the function findLines(F). 
			For example, if F = x^4 + y^4 + z^4, enter
				findLines( x^4 + y^4 + z^4);
		b.) To output the cohomology group H1 of Galois acting on
			the lines as well as the Galois action itself after
			having found the lines, use the function
			findH1WithLines.
			For example after entering
				lines, L := findLines(x^4+y^4+z^4);
			input
				findH1WithLines(lines, L);
		c.) To do it all at once, that is output the lines on X,
			the field of definition for the lines on X, the
			cohomology group H1 of Galois acting on the lines, and
			the Galois action itself, use the function
			findH1WithoutLines.
			For example, enter
				findH1WithoutLines(x^4+y^4+z^4);



FILE: dP2H1.magma
	FUNCTION: findLines
		INPUT: q - homogeneous quartic polynomial in x, y, z over Q
		OUTPUT: lines, L - the list of lines which lie on w^2 = q, 
			the field of definiton for all lines
	FUNCTION: findH1 := function
		INPUT: lines, L - a list of lines on X, the field over 
			which the lines are defined
		OUTPUT: lines, L, H1, GalAction - the list of lines on X,
			the field over which the lines are defined, H1(PicXcl),
			the permutation group of the lines given by Gal(L/Q)
	FUNCTION: findH1WithoutLines 
		INPUT: q - a quartic polynomial in P2
		OUTPUT: lines, L, H1, GalAction - the list of lines on X,
			the field over which the lines are defined, H1(PicXcl),
			the permutation group of the lines given by Gal(L/Q)
	FUNCTION: findH1WithLines 
		INPUT: lines, L - the list of lines on X,
			the field over which the lines are defined
		OUTPUT: H1, GalAction - H1(PicXcl),
			the permutation group of the lines given by Gal(L/Q)

	


FILE: backgroundFunctions.magma
	FUNCTION: getCo
		INPUT: poly, m - a polynomial, a monomial in the polynomial 
			ring containing poly
		OUTPUT: the coefficient of m in poly
	FUNCTION: getEqns
		INPUT: poly - a quartic polynomial in 2 variables
		OUTPUT: the list of equations that must be satisfied  in 
			order for poly to be a square
	FUNCTION: inTermsOfx
		INPUT: q, k - a quartic polynomial in 3 variables, 
			the field over which q is defined
		OUTPUT: the lines of the form x = ay+bz which are 
			bitangent to q
	FUNCTION: inTermsOfy
		INPUT: q, k - a quartic polynomial in 3 variables, 
			the field over which q is defined
		OUTPUT: the lines of the form y = az which are bitangent 
			to q
	FUNCTION: findBitangents
		INPUT: C - a quartic curve (scheme) in P2
		OUTPUT: the lines in P2 which are bitangent to C
	FUNCTION: AutPolyAction 
		INPUT: poly, sigma - a polynomial, an automorphism of the
			field over which poly is defined
		OUTPUT: the result of sigma acting on the 
			coefficients of poly  	
	FUNCTION: AutSchemeAction 
		INPUT: l, sigma - a scheme, an automorphism of the field
			over which l is defined
  		OUTPUT: the scheme given by sigma(l)
	FUNCTION: LAction 
		INPUT: sigma, lines - a field automorphism, a list of
			schemes defined over the field for which sigma is 
			an automorphism
		OUTPUT: a list, LAct, for which LAct[i] is the index
			of sigma(lines[i]) in the list lines.











