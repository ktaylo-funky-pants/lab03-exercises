# lab03-exercises

def find_all_duplicates(l):
	new_list = []
	l.sort()
	seen = set()
	for i in range(len(l)-1):
		if l[i] == l[i+1]:
			if l[i] not in seen:
				new_list.append(l[i])
				seen.add(l[i])
	return new_list 

#explanation of two ways to solve
#Nested, with a nested loop you can loop through every element and compare it to every other element to find duplicates. However this is o(n^2) 
#Dict, with a dict you can add elements to it as you loop through the list, and then check if that element is a already in the dict easy with the o(1) formula,
#if it is already in the dict then you know it is a duplicate. This achieves o(n) as you only need to loop the list once but it can be more difficult to set up 
