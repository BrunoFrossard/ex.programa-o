```javascript
class FilaAtendimento {
  constructor() {
    this.alunos = [];
  }
  adicionarAluno(nome) {
    this.alunos.push(nome);
    console.log(`Aluno ${nome} adicionado à fila de atendimento.`);
  }
  atenderAluno() {
    if (this.alunos.length === 0) {
      console.log("Não há alunos na fila para atender.");
      return null;
    }
    const alunoAtendido = this.alunos.shift();
    console.log(`Aluno ${alunoAtendido} atendido.`);
    return alunoAtendido;
  }
  verProximoAluno() {
    if (this.alunos.length === 0) {
      console.log("Não há alunos na fila.");
      return null;
    }
    const proximo = this.alunos[0];
    console.log(`Próximo aluno a ser atendido: ${proximo}`);
    return proximo;
  }
  mostrarFila() {
    if (this.alunos.length === 0) {
      console.log("A fila de atendimento está vazia.");
      return;
    }
    console.log("Fila de Atendimento:");
    this.alunos.forEach((aluno, index) => {
      console.log(`${index + 1}. ${aluno}`);
    });
  }
}
class PilhaDocumentos {
  constructor() {
    this.documentos = [];
  }
  adicionarDocumento(descricao) {
    this.documentos.push(descricao);
    console.log(`Documento "${descricao}" adicionado à pilha de documentos urgentes.`);
  }
  resolverDocumento() {
    if (this.documentos.length === 0) {
      console.log("Não há documentos para resolver.");
      return null;
    }
    const documentoResolvido = this.documentos.pop();
    console.log(`Documento "${documentoResolvido}" resolvido.`);
    return documentoResolvido;
  }
  verTopoDocumento() {
    if (this.documentos.length === 0) {
      console.log("Não há documentos na pilha.");
      return null;
    }
    const topo = this.documentos[this.documentos.length - 1];
    console.log(`Documento no topo: "${topo}"`);
    return topo;
  }
  mostrarDocumentos() {
    if (this.documentos.length === 0) {
      console.log("A pilha de documentos está vazia.");
      return;
    }
    console.log("Documentos Pendentes (do mais recente ao mais antigo):");
    for (let i = this.documentos.length - 1; i >= 0; i--) {
      console.log(`${this.documentos.length - i}. ${this.documentos[i]}`);
    }
  }
}
```
