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

