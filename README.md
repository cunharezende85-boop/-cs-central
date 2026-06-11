<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Guia de Publicação — GitHub Pages · Central CS</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&family=DM+Mono:wght@400;500&display=swap');
  :root {
    --bg: #0f0f0f; --surface: #1a1a1a; --surface2: #222;
    --border: #2e2e2e; --accent: #f97316; --text: #e8e8e8;
    --muted: #888; --green: #22c55e; --blue: #3b82f6;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: 'DM Sans', sans-serif; background: var(--bg); color: var(--text); padding: 40px 24px 80px; }
  .wrap { max-width: 720px; margin: 0 auto; }

  h1 { font-size: 24px; font-weight: 700; color: var(--accent); margin-bottom: 6px; }
  .subtitle { font-size: 13px; color: var(--muted); margin-bottom: 40px; }

  .step-block { display: flex; gap: 20px; margin-bottom: 28px; }
  .step-num {
    width: 36px; height: 36px; border-radius: 50%;
    background: var(--accent); color: #000;
    font-weight: 700; font-size: 15px;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0; margin-top: 2px;
  }
  .step-body { flex: 1; }
  .step-title { font-size: 15px; font-weight: 600; margin-bottom: 6px; }
  .step-desc { font-size: 13px; color: var(--muted); line-height: 1.7; margin-bottom: 10px; }

  .code-box {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    border-radius: 6px;
    padding: 10px 14px;
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    color: var(--text);
    margin-top: 8px;
    white-space: pre;
  }

  .img-placeholder {
    background: var(--surface);
    border: 1px dashed var(--border);
    border-radius: 8px;
    padding: 20px;
    text-align: center;
    font-size: 12px;
    color: var(--muted);
    margin-top: 10px;
  }

  .alert {
    border-radius: 8px; padding: 12px 16px;
    font-size: 13px; line-height: 1.6;
    margin: 20px 0;
    border-left: 3px solid;
  }
  .alert-orange { background: rgba(249,115,22,.08); border-color: var(--accent); }
  .alert-green  { background: rgba(34,197,94,.08);  border-color: var(--green); }
  .alert-blue   { background: rgba(59,130,246,.08); border-color: var(--blue); }

  .url-box {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 16px 20px;
    margin: 24px 0;
    text-align: center;
  }
  .url-box .label { font-size: 11px; color: var(--muted); text-transform: uppercase; letter-spacing: .08em; margin-bottom: 8px; }
  .url-box .url { font-family: 'DM Mono', monospace; font-size: 15px; color: var(--accent); font-weight: 600; }

  hr { border: none; border-top: 1px solid var(--border); margin: 36px 0; }
  .section-title { font-size: 13px; font-weight: 700; color: var(--accent); text-transform: uppercase; letter-spacing: .08em; margin-bottom: 20px; margin-top: 36px; }

  .tag {
    display: inline-block; padding: 2px 8px; border-radius: 4px;
    font-size: 11px; font-weight: 600;
    background: rgba(249,115,22,.15); color: var(--accent);
    margin-bottom: 4px;
  }
</style>
</head>
<body>
<div class="wrap">

  <h1>Guia de Publicação</h1>
  <p class="subtitle">Como publicar a Central CS no GitHub Pages — passo a passo completo</p>

  <div class="alert alert-blue">
    ℹ️ <strong>Pré-requisito:</strong> você vai precisar de uma conta no GitHub (<strong>cunharezende85-boop</strong>) e do arquivo <code style="background:rgba(59,130,246,.15);padding:1px 5px;border-radius:3px;font-size:11px;">index.html</code> da Central CS no seu computador.
  </div>

  <!-- ══════════════════════════════════════ -->
  <p class="section-title">Parte 1 — Criar o repositório</p>

  <div class="step-block">
    <div class="step-num">1</div>
    <div class="step-body">
      <div class="step-title">Acesse o GitHub e faça login</div>
      <div class="step-desc">Abra <strong>github.com</strong> no navegador e entre com a conta <strong>cunharezende85-boop</strong>.</div>
    </div>
  </div>

  <div class="step-block">
    <div class="step-num">2</div>
    <div class="step-body">
      <div class="step-title">Crie um novo repositório</div>
      <div class="step-desc">No canto superior direito, clique no ícone <strong>+</strong> e selecione <strong>"New repository"</strong>.</div>
    </div>
  </div>

  <div class="step-block">
    <div class="step-num">3</div>
    <div class="step-body">
      <div class="step-title">Configure o repositório</div>
      <div class="step-desc">Preencha exatamente assim:</div>
      <div class="code-box">Repository name:  cs-central
Description:      Central Unificada de Customer Success — Pós-Graduação & MBA
Visibility:       ✅ Public   (obrigatório para GitHub Pages gratuito)
Initialize:       ✅ Add a README file</div>
      <div class="step-desc" style="margin-top:10px;">Clique em <strong>"Create repository"</strong>.</div>
    </div>
  </div>

  <!-- ══════════════════════════════════════ -->
  <hr>
  <p class="section-title">Parte 2 — Fazer upload dos arquivos</p>

  <div class="step-block">
    <div class="step-num">4</div>
    <div class="step-body">
      <div class="step-title">Abra o repositório criado</div>
      <div class="step-desc">Você estará na tela principal do repositório. Clique em <strong>"Add file"</strong> → <strong>"Upload files"</strong>.</div>
    </div>
  </div>

  <div class="step-block">
    <div class="step-num">5</div>
    <div class="step-body">
      <div class="step-title">Arraste os 3 arquivos para a área de upload</div>
      <div class="step-desc">Você baixou um arquivo .zip com 3 arquivos. Arraste todos para a área de upload no GitHub:</div>
      <div class="code-box">index.html      ← arquivo principal da Central CS
README.md       ← descrição do repositório  
.nojekyll       ← garante que o GitHub Pages sirva o HTML corretamente</div>
      <div class="step-desc" style="margin-top:10px;">⚠️ O arquivo <strong>.nojekyll</strong> pode não aparecer no seu gerenciador de arquivos porque começa com ponto. Se isso acontecer, crie ele manualmente no GitHub (Passo 6 abaixo).</div>
    </div>
  </div>

  <div class="step-block">
    <div class="step-num">6</div>
    <div class="step-body">
      <div class="step-title">Criar .nojekyll manualmente (se necessário)</div>
      <div class="step-desc">Se o .nojekyll não apareceu, crie direto no GitHub: clique em <strong>"Add file"</strong> → <strong>"Create new file"</strong>, coloque o nome <code style="font-family:monospace;">.nojekyll</code>, deixe o conteúdo vazio e salve com commit.</div>
    </div>
  </div>

  <div class="step-block">
    <div class="step-num">7</div>
    <div class="step-body">
      <div class="step-title">Confirme o commit</div>
      <div class="step-desc">Role a página para baixo. Em <strong>"Commit changes"</strong>, deixe a mensagem padrão ou escreva <code style="font-family:monospace;">Publicação inicial — Central CS v1.1</code>. Clique em <strong>"Commit changes"</strong>.</div>
    </div>
  </div>

  <!-- ══════════════════════════════════════ -->
  <hr>
  <p class="section-title">Parte 3 — Ativar o GitHub Pages</p>

  <div class="step-block">
    <div class="step-num">8</div>
    <div class="step-body">
      <div class="step-title">Acesse as configurações do repositório</div>
      <div class="step-desc">No menu superior do repositório, clique em <strong>Settings</strong> (ícone de engrenagem).</div>
    </div>
  </div>

  <div class="step-block">
    <div class="step-num">9</div>
    <div class="step-body">
      <div class="step-title">Ative o GitHub Pages</div>
      <div class="step-desc">No menu lateral esquerdo, clique em <strong>Pages</strong>. Em <strong>"Source"</strong>, selecione:</div>
      <div class="code-box">Branch:  main
Folder:  / (root)</div>
      <div class="step-desc" style="margin-top:10px;">Clique em <strong>"Save"</strong>.</div>
    </div>
  </div>

  <div class="step-block">
    <div class="step-num">10</div>
    <div class="step-body">
      <div class="step-title">Aguarde ~1 minuto</div>
      <div class="step-desc">O GitHub vai construir o site. Atualize a página de Settings → Pages até aparecer a mensagem verde: <strong>"Your site is live at…"</strong></div>
    </div>
  </div>

  <!-- ══════════════════════════════════════ -->
  <hr>
  <p class="section-title">✅ Resultado final</p>

  <div class="url-box">
    <div class="label">URL pública da Central CS</div>
    <div class="url">https://cunharezende85-boop.github.io/cs-central/</div>
  </div>

  <div class="alert alert-green">
    ✅ Qualquer pessoa com o link consegue abrir a Central CS no navegador — sem login, sem instalar nada. Funciona no celular, tablet e computador.
  </div>

  <!-- ══════════════════════════════════════ -->
  <hr>
  <p class="section-title">🔄 Como atualizar a Central no futuro</p>

  <div class="step-block">
    <div class="step-num">1</div>
    <div class="step-body">
      <div class="step-title">Acesse o repositório no GitHub</div>
      <div class="step-desc">github.com/cunharezende85-boop/cs-central</div>
    </div>
  </div>

  <div class="step-block">
    <div class="step-num">2</div>
    <div class="step-body">
      <div class="step-title">Clique no arquivo index.html</div>
      <div class="step-desc">Depois clique no ícone de lápis ✏️ para editar, ou clique em <strong>"..."</strong> → <strong>"Upload new version"</strong> para substituir o arquivo inteiro.</div>
    </div>
  </div>

  <div class="step-block">
    <div class="step-num">3</div>
    <div class="step-body">
      <div class="step-title">Confirme o commit</div>
      <div class="step-desc">Salve com uma mensagem descritiva, ex: <code style="font-family:monospace;">Atualização — novo curso adicionado</code>. O site é atualizado automaticamente em ~1 minuto.</div>
    </div>
  </div>

  <div class="alert alert-orange">
    💡 <strong>Dica:</strong> o link <strong>nunca muda</strong>. Você pode compartilhar uma vez com o time e qualquer atualização futura já aparece automaticamente para todos.
  </div>

  <!-- ══════════════════════════════════════ -->
  <hr>
  <p class="section-title">📱 Como compartilhar com o time</p>

  <div class="step-block">
    <div class="step-num">💬</div>
    <div class="step-body">
      <div class="step-title">Mensagem pronta para o grupo do time</div>
      <div class="code-box">Pessoal! A Central de CS está disponível online agora. 🎉

Acesse pelo link abaixo — funciona no celular e no computador, sem precisar baixar nada:

👉 https://cunharezende85-boop.github.io/cs-central/

Lá estão todos os fluxos, templates, FAQ, checklist, pipeline e o banco de mensagens com variações prontas para usar no WhatsApp. 

Qualquer dúvida, chama o Junior!</div>
    </div>
  </div>

</div>
</body>
</html>
