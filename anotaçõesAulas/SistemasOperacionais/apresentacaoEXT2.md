---
marp: true
theme: gradient
class:  
- blue
- lead
paginate: true
---

# **Sistema de Arquivos - EXT2**
## Sistemas Operacionais - Engenharia de Software e Ciência da Computação`
### **Stéfani Arnold e Nicolas Hass**
### `Módulo 02/2024`
```python
batata = 10
print(batata)
```

---

# **Definição**
- **ext2**: Sistema de arquivos de segunda extensão para sistemas `Linux`.
- **Características**: Simplicidade e eficiência.

---

# Sistemas Operacionais e Versões
- **Usado em**: Distribuições Linux mais antigas, como `Slackware, Debian e Red Hat`.
- **Versões do Kernel**: Disponível a partir do Linux Kernel 2.0.

---

### **Localização dentro da Partição**
- **Estrutura**: 
  - Superbloco
  - Grupos de blocos
  - Inodes e tabelas de blocos
- **Montagem**: Localizado na partição onde o sistema de arquivos é montado.

---

### Tipo de Alocação
- **Alocação**: Contígua, utilizando `bitmap` para rastrear blocos e inodes livres.

---

### **Implementação de Diretórios**
- **Diretórios**: 
  - Listas encadeadas de entradas de diretório.
  - Cada entrada contém nome do arquivo e número do inode.

---

### Nome e Permissões de Arquivos
- **Nome de Arquivo**: Até 255 caracteres.
- **Permissões**: Modelo Unix – leitura, escrita e execução para usuário, grupo e outros.

---

### **Capacidade e Tamanho**
- **Tamanho do Bloco**: 1 KB, 2 KB ou 4 KB.
- **Tamanho Máximo de Arquivo**: Até 2 TB (com blocos de 4 KB).
- **Journaling**: Não possui.

---

### Vantagens
- Simples e eficiente.
- Baixo consumo de `CPU` e memória.
- Boa performance em discos menores.

---

### **Desvantagens**
- Sem suporte para journaling – problemas de consistência após falhas.
- Limitações de tamanho de arquivo comparado com ext3/ext4.

---

### Melhores Usos
- **Ambientes Simples**: Prioriza simplicidade e baixa demanda de recursos.
- **Dispositivos Embarcados**: Eficiente em sistemas com recursos limitados.
- **Sistemas com Backups Regulares**: Minimiza risco de perda de dados.

---

### **Referências**
- GARRELS, M. The Linux Documentation Project. Disponível em: <https://tldp.org/>. Acesso em: 5 nov. 2024.
- CORBET, J. et al. The second extended filesystem — the Linux kernel documentation. Disponível em: <https://www.kernel.org/doc/html/latest/filesystems/ext2.html>. Acesso em: 5 nov. 2024.
- KERRISK, M. ext4(5) - Linux manual page. Disponível em: <https://man7.org/linux/man-pages/man5/ext2.5.html>. Acesso em: 5 nov. 2024.

---

# `Perguntas?`

stefani.camargo@sou.unijui.edu.br



