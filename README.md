# CpG-Island-Counter
Config files for my GitHub profile.
dna = '''ATCG'''
cg_count = dna.count("CG")
gc_count = dna.count("GC")
tg_count = dna.count("TG")
c_count = dna.count("C")
t_count = dna.count ("T")
a_count = dna.count ("A")
g_count = dna.count ("G")
total_nuc = len(dna) 
cg_percent = (cg_count/total_nuc)*100
gc_percent = (gc_count/total_nuc)*100
tg_percent = (tg_count/total_nuc)*100
c_percent = (c_count/total_nuc)*100
t_percent = (t_count/total_nuc)*100
a_percent = (a_count/total_nuc)*100
g_percent = (g_count/total_nuc)*100
def calcular_gc(sequencia):
    # Converte para maiúsculas para evitar erros
    seq = sequencia.upper()
    
    # Conta G e C
    contagem_g = seq.count('G')
    contagem_c = seq.count('C')
    
    # Conta total de bases
    total_bases = len(seq)
    
    # Calcula a porcentagem, evitando divisão por zero
    if total_bases == 0:
        return 0.0
    
    gc_percentual = ((contagem_g + contagem_c) / total_bases) * 100
    return gc_percentual
resultado = calcular_gc(dna)
CGGCratio = (cg_count/gc_count)
print("lenght = ", len(dna))
print(f"GC%: {resultado:.2f}")
print("CG% =", cg_percent)
print("CGGCratio =", CGGCratio)
print("TG% =", tg_percent)
print("C% = ", c_percent)
print("T% = ", t_percent)
print("A% = ", a_percent)
print("G% = ", g_percent)
print("CG = ", cg_count)
#find CpG island looping through the sequence DNA
for i in range(len(dna) -1):
    if dna[i:i+2] == "CG":
        print("CpG at:", i + 1)
