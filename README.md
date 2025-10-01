<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Agent Immobilier Augmenté – IA pour pros | Landing</title>
  <meta name="description" content="Analyse d'annonces par IA, comparateur PDF, générateur d'e-mails, fiches clients, boîte à outils – avec abonnements PayPal et essai gratuit." />
  <style>
    :root{
      --bg:#243b55;
      --panel:#7392e0;          /* bleu pervenche */
      --primary:#e91e63;        /* rose */
      --accent:#4fa3f7;         /* bleu ciel */
      --navy:#1a2a4f;           /* bleu foncé */
      --ink:#0e1420;
      --text:#ffffff;
      --muted:#bcd1ff;
      --card:#eef4ff;
      --radius:14px;
      --shadow:0 10px 24px rgba(0,0,0,.25);
    }
    *{box-sizing:border-box}
    html,body{margin:0;background:var(--bg);color:var(--text);font:16px/1.5 'Segoe UI',system-ui,-apple-system,Roboto,Arial,sans-serif}
    a{color:inherit}
    img{max-width:100%;display:block}

    /* Layout */
    .wrap{max-width:1200px;margin-inline:auto;padding-inline:24px}

    /* Header */
    header{position:sticky;top:0;z-index:30;background:linear-gradient(180deg, rgba(18,27,46,.9), rgba(36,59,85,.85));backdrop-filter:saturate(140%) blur(6px);border-bottom:1px solid rgba(255,255,255,.08)}
    .nav{display:flex;align-items:center;gap:18px;min-height:68px}
    .brand{display:flex;align-items:center;gap:10px;font-weight:800;letter-spacing:.3px}
    .brand .logo{width:30px;height:30px;display:grid;place-items:center;border-radius:9px;background:var(--primary);box-shadow:0 6px 14px rgba(233,30,99,.4)}
    .spacer{flex:1}
    .nav a{font-weight:600;opacity:.92;text-decoration:none;padding:8px 12px;border-radius:8px}
    .nav a:hover{background:rgba(255,255,255,.08)}
    .cta{background:var(--primary);color:#fff;padding:10px 16px;border-radius:10px;font-weight:800;text-decoration:none;box-shadow:0 8px 18px rgba(233,30,99,.35)}

    /* Hero */
    .hero{position:relative;overflow:hidden;padding:80px 0 50px}
    .hero::before{content:"";position:absolute;inset:-20% -10% auto -10%;height:70%;background:radial-gradient(1200px 400px at 50% -10%, rgba(79,163,247,.35), transparent 60%), radial-gradient(900px 300px at 10% 10%, rgba(233,30,99,.25), transparent 60%)}
    .hero h1{margin:0 0 10px;font-size:40px;line-height:1.15;text-align:center}
    .hero p{color:var(--muted);text-align:center;margin:0 auto 22px;max-width:780px}
    .hero .actions{display:flex;gap:14px;justify-content:center;flex-wrap:wrap}
    .btn{display:inline-flex;align-items:center;gap:10px;padding:12px 18px;border-radius:12px;text-decoration:none;font-weight:700;border:1px solid transparent}
    .btn.primary{background:var(--primary);color:#fff;box-shadow:0 10px 18px rgba(233,30,99,.35)}
    .btn.secondary{background:var(--navy);border-color:rgba(255,255,255,.1)}

    /* Video */
    .video-card{background:var(--panel);border-radius:var(--radius);box-shadow:var(--shadow);padding:18px}
    .video-embed{position:relative;padding-top:56.25%;border-radius:12px;overflow:hidden;border:2px solid rgba(0,0,0,.15);background:#000}
    .video-embed iframe{position:absolute;inset:0;width:100%;height:100%;border:0}

    /* Feature grid */
    .section{padding:50px 0}
    .section h2{margin:0 0 18px;font-size:28px}
    .grid{display:grid;gap:18px}
    @media(min-width:820px){.grid.cols-3{grid-template-columns:repeat(3,1fr)}.grid.cols-2{grid-template-columns:repeat(2,1fr)}}
    .card{background:var(--panel);border-radius:var(--radius);box-shadow:var(--shadow);padding:22px;border:1px solid rgba(255,255,255,.06)}
    .card h3{margin:6px 0 8px;font-size:20px}
    .chip{display:inline-flex;align-items:center;gap:8px;background:rgba(255,255,255,.1);border:1px solid rgba(255,255,255,.15);padding:6px 10px;border-radius:999px;font-weight:700}

    /* Steps */
    .steps{display:grid;gap:18px}
    @media(min-width:900px){.steps{grid-template-columns:repeat(3,1fr)}}
    .step{background:linear-gradient(180deg, rgba(115,146,224,.9), rgba(115,146,224,.75));padding:18px;border-radius:14px;border:1px solid rgba(255,255,255,.1)}
    .step .num{width:34px;height:34px;border-radius:50%;display:grid;place-items:center;background:var(--primary);font-weight:800;margin-bottom:10px;box-shadow:0 6px 12px rgba(233,30,99,.35)}

    /* Pricing */
    .pricing{display:grid;gap:18px}
    @media(min-width:980px){.pricing{grid-template-columns:repeat(3,1fr)}}
    .price-card{background:var(--panel);border-radius:var(--radius);box-shadow:var(--shadow);padding:22px;border:1px solid rgba(255,255,255,.08);position:relative}
    .price-badge{position:absolute;top:12px;right:12px;background:var(--primary);padding:6px 10px;border-radius:999px;font-size:12px;font-weight:800}
    .price{font-size:34px;font-weight:900;margin:10px 0}
    .price small{font-size:14px;color:var(--ink);opacity:.8}
    .ul{margin:12px 0 0;padding:0;list-style:none}
    .ul li{margin:10px 0;display:flex;gap:10px;align-items:flex-start}
    .ul li i{color:#9ff3c8}

    /* Testimonials */
    .testis{display:grid;gap:18px}
    @media(min-width:900px){.testis{grid-template-columns:repeat(3,1fr)}}
    .quote{background:var(--panel);border-radius:var(--radius);padding:18px;box-shadow:var(--shadow)}
    .row{display:flex;align-items:center;gap:12px;margin-top:12px}
    .avatar{width:44px;height:44px;border-radius:50%;background:linear-gradient(135deg, var(--accent), var(--primary));display:grid;place-items:center;font-weight:800}

    /* FAQ */
    details{background:var(--panel);border-radius:var(--radius);padding:14px 16px;box-shadow:var(--shadow);border:1px solid rgba(255,255,255,.08)}
    details+details{margin-top:12px}
    summary{cursor:pointer;font-weight:800}

    /* Footer */
    footer{padding:40px 0;background:linear-gradient(180deg, var(--navy), #0c1530)}
    .socials{display:flex;gap:12px}
    .socials a{width:38px;height:38px;border-radius:10px;background:rgba(255,255,255,.08);display:grid;place-items:center;text-decoration:none}
    .badge{display:inline-flex;gap:8px;align-items:center;background:rgba(255,255,255,.08);border:1px solid rgba(255,255,255,.15);padding:8px 10px;border-radius:12px}

    /* Helpers */
    .center{text-align:center}
    .muted{color:var(--muted)}
    .mt-20{margin-top:20px}
    .mt-30{margin-top:30px}
    .mb-10{margin-bottom:10px}
    .mb-20{margin-bottom:20px}
  </style>
  
  <!-- Meta Pixel + Consent helpers -->
  <script>
    const CONSENT_KEY = 'consent_prefs_v1';
    function getConsent(){ try{return JSON.parse(localStorage.getItem(CONSENT_KEY)||'null');}catch(e){return null;} }
    function setConsent(prefs){ localStorage.setItem(CONSENT_KEY, JSON.stringify(prefs)); const b=document.getElementById('cookie-banner'); if(b) b.style.display='none'; if(prefs && prefs.marketing){ loadMetaPixel(); } }
    function loadMetaPixel(){ if(window.fbqLoaded) return; window.fbqLoaded=true; !function(f,b,e,v,n,t,s){if(f.fbq)return;n=f.fbq=function(){n.callMethod? n.callMethod.apply(n,arguments):n.queue.push(arguments)};if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';n.queue=[];t=b.createElement(e);t.async=!0;t.src=v;s=b.getElementsByTagName(e)[0];s.parentNode.insertBefore(t,s)}(window, document,'script','https://connect.facebook.net/en_US/fbevents.js');
      try{ fbq('init','META_PIXEL_ID'); fbq('track','PageView'); }catch(e){}
    }
    document.addEventListener('DOMContentLoaded',()=>{ const c=getConsent(); if(!c){ const b=document.getElementById('cookie-banner'); if(b) b.style.display='flex'; } else if(c.marketing){ loadMetaPixel(); } });
  </script>
  <style>
    #cookie-banner{position:fixed;z-index:9999;left:16px;right:16px;bottom:16px;display:none;align-items:flex-start;gap:16px;background:var(--navy);color:#fff;border:1px solid rgba(255,255,255,.15);border-radius:12px;box-shadow:var(--shadow);padding:14px 16px}
    #cookie-banner .txt{flex:1;color:var(--muted)}
    #cookie-banner .actions{display:flex;gap:10px;flex-wrap:wrap}
    #cookie-banner button{border:none;border-radius:10px;padding:10px 14px;font-weight:800;cursor:pointer}
    #cookie-accept{background:var(--primary);color:#fff;box-shadow:0 6px 14px rgba(233,30,99,.35)}
    #cookie-decline{background:rgba(255,255,255,.08);color:#fff;border:1px solid rgba(255,255,255,.18)}
  </style>
  <style>
    /* Modals légales */
    .modal{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:rgba(6,10,20,.6);z-index:9998;padding:20px}
    .modal[open]{display:flex}
    .modal-card{max-width:900px;width:100%;background:var(--panel);color:#fff;border-radius:14px;border:1px solid rgba(255,255,255,.12);box-shadow:var(--shadow);overflow:hidden}
    .modal-head{display:flex;align-items:center;justify-content:space-between;background:var(--navy);padding:12px 16px}
    .modal-head h3{margin:0;font-size:20px}
    .modal-body{padding:18px;max-height:min(70vh,720px);overflow:auto}
    .modal-close{background:var(--primary);color:#fff;border:none;border-radius:10px;padding:8px 12px;font-weight:800;cursor:pointer}
    .modal-body h4{margin:14px 0 6px}
    .modal-body p,.modal-body li{color:#eef4ff}
    .legal-small{font-size:13px;color:var(--muted)}
  </style>
</head>
<body>
  <header>
    <div class="wrap nav">
      <div class="brand"><span class="logo">🏠</span> <span>Agent Immobilier augmenté</span></div>
      <div class="spacer"></div>
      <a href="#features">Fonctionnalités</a>
      <a href="#pricing">Tarifs</a>
      <a href="#video">Demo</a>
      <a href="#temoignages">Avis</a>
      <a href="#newsletter">Newsletter</a>
      <a class="cta" href="#pricing">Démarrer l'essai gratuit</a>
    </div>
  </header>

  <section class="hero wrap">
    <h1>Vendez plus vite avec votre <span style="color:var(--primary)">assistant IA</span> tout-en-un</h1>
    <p>Analyse d'annonces par IA, comparaison de PDF, génération d'e-mails, fiches clients et boîte à outils. Intégration PayPal, webhooks, et quotas adaptés à votre activité.</p>
    <div class="actions mt-20">
      <a href="#pricing" class="btn primary">🚀 Démarrer 30 jours gratuits</a>
      <a href="#video" class="btn secondary">▶️ Regarder la démo</a>
    </div>
  </section>

  <section id="video" class="wrap section">
    <div class="video-card">
      <div class="video-embed">
        <!-- Remplacez l'URL YouTube/Vimeo ci-dessous -->
        <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="Demo produit" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
    </div>
  </section>

  <section id="features" class="wrap section">
    <h2>Tout ce qu'il faut pour une vente parfaite</h2>
    <div class="grid cols-3 mt-20">
      <div class="card"><div class="chip">🤖 Analyse IA</div><h3>Analyse d'annonce</h3><p class="muted">Collez l'URL ou le code source et laissez l'IA sortir les points forts, faiblesses et recommandations.</p></div>
      <div class="card"><div class="chip">📑 PDF</div><h3>Comparateur PDF IA</h3><p class="muted">Comparez diagnostics, estimations, mandats… en quelques secondes.</p></div>
      <div class="card"><div class="chip">✉️ Emails</div><h3>Générateur d'e-mails</h3><p class="muted">Modèles prêts à l'emploi pour chaque étape (R0 → Acte) avec fusion client/adresse/date.</p></div>
      <div class="card"><div class="chip">🗂️ CRM</div><h3>Fiches clients</h3><p class="muted">Suivi simple : étape, statut, rendez-vous, documents joints et export PDF.</p></div>
      <div class="card"><div class="chip">🧰 Outils</div><h3>Boîte à outils</h3><p class="muted">Procédures, légal, scripts d'appel… tous vos liens utiles au même endroit.</p></div>
      <div class="card"><div class="chip">🔒 Paiements</div><h3>PayPal & webhooks</h3><p class="muted">Abonnements sécurisés, activation automatique et facturation simple.</p></div>
    </div>
  </section>

  <section class="wrap section">
    <h2>Comment ça marche à l'usage ?</h2>
    <div class="steps mt-20">
      <div class="step"><div class="num">1</div><h3>Créez votre compte</h3><p class="muted">Activez l'essai 30 jours (10 requêtes) et connectez votre PayPal pour passer au mois/année.</p></div>
      <div class="step"><div class="num">2</div><h3>Centralisez vos actions</h3><p class="muted">Analyse IA, comparaison PDF, mails types, fiches clients… tout est au même endroit.</p></div>
      <div class="step"><div class="num">3</div><h3>Vendez plus vite</h3><p class="muted">Des décisions rapides, des mails pro, et des dossiers carrés qui inspirent confiance.</p></div>
    </div>
  </section>

  <section id="pricing" class="wrap section">
    <h2>Des tarifs simples, pensés pour l'immobilier</h2>
    <div class="pricing mt-20">
      <div class="price-card">
        <span class="price-badge">Essai 30j</span>
        <h3>Gratuit</h3>
        <div class="price">0€ <small>/ 30 jours</small></div>
        <ul class="ul">
          <li><i>✔</i> 10 requêtes IA</li>
          <li><i>✔</i> Accès complet aux outils</li>
          <li><i>✔</i> Export PDF</li>
        </ul>
        <div id="paypal-trial" class="mt-20"></div>
        <a href="#" class="btn secondary mt-20" onclick="alert('Remplacez TRIAL_PLAN_ID et votre client-id PayPal pour activer.');return false;">Activer l'essai</a>
      </div>

      <div class="price-card" style="outline:2px solid rgba(233,30,99,.35)">
        <span class="price-badge">Le + populaire</span>
        <h3>Mensuel</h3>
        <div class="price">8,90€ <small>/ mois</small></div>
        <ul class="ul">
          <li><i>✔</i> 100 requêtes / mois</li>
          <li><i>✔</i> Support prioritaire</li>
          <li><i>✔</i> Tous les modules inclus</li>
        </ul>
        <div id="paypal-monthly" class="mt-20"></div>
        <a href="#" class="btn primary mt-20" onclick="alert('Remplacez MONTHLY_PLAN_ID et votre client-id PayPal pour activer.');return false;">S'abonner</a>
      </div>

      <div class="price-card">
        <h3>Annuel</h3>
        <div class="price">95€ <small>/ an</small></div>
        <ul class="ul">
          <li><i>✔</i> Requêtes illimitées</li>
          <li><i>✔</i> 2 mois offerts</li>
          <li><i>✔</i> Accès à toutes les nouveautés</li>
        </ul>
        <div id="paypal-yearly" class="mt-20"></div>
        <a href="#" class="btn secondary mt-20" onclick="alert('Remplacez YEARLY_PLAN_ID et votre client-id PayPal pour activer.');return false;">Payer l'année</a>
      </div>
    </div>
    <p class="muted mt-20">Paiement sécurisé via PayPal. Résiliation en 1 clic. Webhook prêt pour l'activation automatique (remplacez les IDs dans le code).</p>
  </section>

  <section id="temoignages" class="wrap section">
    <h2>Ils recommandent ✨</h2>
    <div class="testis mt-20">
      <div class="quote"><p>"En 48h j'avais un dossier nickel pour une offre. Les mails types + l'analyse IA = gain de temps de fou."</p><div class="row"><div class="avatar">AG</div><div><strong>Aurélie G.</strong><div class="muted">Mandataire, Lyon</div></div></div></div>
      <div class="quote"><p>"Le comparateur PDF m'a évité une erreur coûteuse sur un diagnostic. ROI dès le 1er mois."</p><div class="row"><div class="avatar">MV</div><div><strong>Martin V.</strong><div class="muted">Agence, Nantes</div></div></div></div>
      <div class="quote"><p>"Top pour la prospection : j'utilise les mails et la fiche client à chaque lead."</p><div class="row"><div class="avatar">SD</div><div><strong>Sonia D.</strong><div class="muted">Indépendante, Nice</div></div></div></div>
    </div>
  </section>

  <section class="wrap section">
    <h2>Questions fréquentes</h2>
    <details class="mt-20"><summary>Comment fonctionnent les requêtes IA ?</summary><p class="muted">Chaque analyse d'annonce ou comparaison PDF consomme 1 requête. Le plan annuel est illimité.</p></details>
    <details><summary>Puis-je résilier quand je veux ?</summary><p class="muted">Oui, depuis votre espace abonneé (PayPal). L'accès reste actif jusqu'à la fin de la période.</p></details>
    <details><summary>Les paiements sont-ils sécurisés ?</summary><p class="muted">Oui – PayPal gère l'authentification et la facturation. Nos webhooks activent l'accès automatiquement.</p></details>
  </section>

  <!-- Newsletter -->
  <section id="newsletter" class="wrap section">
    <h2>Recevez nos mises à jour et astuces 📨</h2>
    <p class="muted">Une à deux fois par mois, pas de spam. Désinscription en un clic.</p>
    <form id="nl-form" class="mt-20" onsubmit="return false" style="display:flex;gap:10px;flex-wrap:wrap">
      <input type="email" id="nl-email" required placeholder="Votre email" aria-label="Email" style="flex:1;min-width:260px;padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,.2);background:#fff;color:#1a2a4f" />
      <button class="btn primary" id="nl-submit" type="submit">S'inscrire</button>
    </form>
    <div id="nl-msg" class="mt-20 muted" style="display:none">Merci ! Vérifiez votre boîte mail pour confirmer votre inscription.</div>
  </section>

  <footer>
    <div class="wrap" style="display:grid;gap:24px;grid-template-columns:1.2fr .8fr">
      <div>
        <h3>Agent Immobilier augmenté</h3>
        <p class="muted">Conçu pour les pros de l'immobilier : rapide, simple et efficace.</p>
        <div class="badge mt-10">🔐 Paiement sécurisé PayPal</div>
      </div>
      <div>
        <h3>Nous suivre</h3>
        <div class="socials mt-10">
          <a href="#" aria-label="Twitter">🐦</a>
          <a href="#" aria-label="LinkedIn">in</a>
          <a href="#" aria-label="YouTube">▶️</a>
          <a href="#" aria-label="Facebook">f</a>
        </div>
        <p class="muted mt-20">Support : <a href="mailto:support@votre-domaine.com">support@votre-domaine.com</a></p>
      </div>
    </div>
    <div class="wrap" style="margin-top:14px;display:flex;justify-content:space-between;gap:12px;color:#9fb0c3;font-size:14px">
      <div>© <span id="y"></span> Votre Société. Tous droits réservés.</div>
      <div style="display:flex;gap:14px">
        <a href="https://www.iubenda.com/" target="_blank" rel="noopener">CGU</a>
        <a href="https://daveisa88.github.io/landingpage-immo-loi/confidentialite.html">Confidentialité</a>
        <a href="https://daveisa88.github.io/landingpage-immo-loi/mentions-legales.html">Mentions légales</a>

      </div>
    </div>
  </footer>

  <!-- Cookie banner -->
  <div id="cookie-banner" role="dialog" aria-live="polite">
    <div class="txt">Nous utilisons des cookies essentiels pour le site et, avec votre accord, des cookies marketing pour mesurer et améliorer nos campagnes.</div>
    <div class="actions">
      <button id="cookie-decline" onclick="setConsent({essential:true,marketing:false})">Refuser</button>
      <button id="cookie-accept" onclick="setConsent({essential:true,marketing:true})">Accepter</button>
    </div>
  </div>

  <!-- PayPal SDK: remplacez YOUR_CLIENT_ID -->
  <script src="https://www.paypal.com/sdk/js?client-id=YOUR_CLIENT_ID&vault=true&intent=subscription&currency=EUR"></script>
  <script>
    // Rendre l'année
    document.getElementById('y').textContent = new Date().getFullYear();

    // Rendu des boutons PayPal (remplacez les IDs par vos plan_id)
    const PLANS = {
      TRIAL: 'TRIAL_PLAN_ID',     // essai 30j
      MONTHLY: 'MONTHLY_PLAN_ID', // 8.90€/mois
      YEARLY: 'YEARLY_PLAN_ID'    // 95€/an
    };

    function renderPayPal(containerId, planId){
      if(!window.paypal || !planId || planId.includes('PLAN_ID')) return; // pas configuré
      paypal.Buttons({
        style:{color:'blue',shape:'pill',layout:'vertical',label:'subscribe'},
        createSubscription: function(data, actions){ return actions.subscription.create({ plan_id: planId }); },
        onApprove: function(data, actions){
          // TODO: appel webhook / activation côté serveur
          alert('Merci ! Abonnement actif : ' + data.subscriptionID);
        }
      }).render('#'+containerId);
    }

    renderPayPal('paypal-trial', PLANS.TRIAL);
    renderPayPal('paypal-monthly', PLANS.MONTHLY);
    renderPayPal('paypal-yearly', PLANS.YEARLY);
  </script>
  
  <!-- Modals légales -->
  <div class="modal" id="modal-cgu" aria-hidden="true" role="dialog" aria-label="Conditions Générales d'Utilisation">
    <div class="modal-card">
      <div class="modal-head"><h3>Conditions Générales d'Utilisation (CGU)</h3><button class="modal-close" data-close>Fermer</button></div>
      <div class="modal-body">
        <p class="legal-small">Dernière mise à jour : <span id="cgu-date"></span></p>
        <h4>1. Objet</h4>
        <p>Les présentes CGU encadrent l’accès et l’utilisation du service « Agent Immobilier augmenté ».</p>
        <h4>2. Compte & Accès</h4>
        <ul><li>Vous êtes responsable de la confidentialité de vos identifiants.</li><li>L’essai gratuit donne droit à 10 requêtes IA sur 30 jours.</li></ul>
        <h4>3. Abonnements</h4>
        <p>Mensuel (8,90€) et Annuel (95€). Facturation via PayPal, renouvellement tacite résiliable à tout moment.</p>
        <h4>4. Propriété intellectuelle</h4>
        <p>Les contenus, marques et logiciels restent la propriété de l’éditeur.</p>
        <h4>5. Responsabilité</h4>
        <p>Les résultats IA sont fournis à titre d’aide à la décision. Vous conservez l’entière responsabilité des décisions et communications.</p>
      </div>
    </div>
  </div>

  <div class="modal" id="modal-privacy" aria-hidden="true" role="dialog" aria-label="Politique de confidentialité">
    <div class="modal-card">
      <div class="modal-head"><h3>Politique de confidentialité</h3><button class="modal-close" data-close>Fermer</button></div>
      <div class="modal-body">
        <p class="legal-small">Conforme RGPD – Responsable de traitement : <strong>Votre Société</strong> – contact : <a href="mailto:support@votre-domaine.com">support@votre-domaine.com</a></p>
        <h4>Données collectées</h4>
        <ul><li>Email (newsletter), données de paiement (via PayPal), journaux d’usage.</li><li>Cookies essentiels & marketing (avec consentement).</li></ul>
        <h4>Finalités</h4>
        <ul><li>Fourniture du service, support client, facturation.</li><li>Mesure d’audience & publicité si consentement.</li></ul>
        <h4>Vos droits</h4>
        <p>Accès, rectification, suppression, opposition : écrivez-nous à l’adresse ci-dessus. Suppression compte sous 30 jours (hors obligations légales).</p>
        <h4>Sous-traitants</h4>
        <p>PayPal (paiement), Mailchimp (emailing). Hébergeur : à renseigner.</p>
      </div>
    </div>
  </div>

  <div class="modal" id="modal-mentions" aria-hidden="true" role="dialog" aria-label="Mentions légales">
    <div class="modal-card">
      <div class="modal-head"><h3>Mentions légales</h3><button class="modal-close" data-close>Fermer</button></div>
      <div class="modal-body">
        <p><strong>Éditeur :</strong> Votre Société – Adresse – SIREN – Email : support@votre-domaine.com</p>
        <p><strong>Directeur de la publication :</strong> Nom & prénom</p>
        <p><strong>Hébergeur :</strong> Raison sociale – Adresse – Téléphone</p>
        <p><strong>Propriété intellectuelle :</strong> Toute reproduction non autorisée est interdite.</p>
      </div>
    </div>
  </div>

  <script>
    // Modals open/close
    function bindModals(){
      const openers = document.querySelectorAll('[data-modal]');
      openers.forEach(a=>a.addEventListener('click',e=>{e.preventDefault();const id=a.getAttribute('data-modal');const m=document.getElementById('modal-'+id);if(m){m.setAttribute('open','');m.setAttribute('aria-hidden','false');}}));
      document.querySelectorAll('[data-close]').forEach(b=>b.addEventListener('click',()=>{b.closest('.modal').removeAttribute('open');b.closest('.modal').setAttribute('aria-hidden','true');}));
      document.querySelectorAll('.modal').forEach(m=>m.addEventListener('click',e=>{if(e.target===m){m.removeAttribute('open');m.setAttribute('aria-hidden','true');}}));
      document.addEventListener('keydown',e=>{if(e.key==='Escape'){document.querySelectorAll('.modal[open]').forEach(m=>{m.removeAttribute('open');m.setAttribute('aria-hidden','true');});}});
      // date maj CGU
      const d=new Date(); document.getElementById('cgu-date').textContent=d.toLocaleDateString('fr-FR');
    }
    document.addEventListener('DOMContentLoaded',bindModals);
  </script>

</body>
</html>
