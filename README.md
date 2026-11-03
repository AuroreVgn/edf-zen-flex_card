# ⚡ EDF Zen Flex Card — dépôt historique

> [!IMPORTANT]
> **EDF Zen Flex Card est désormais intégrée directement au code de l'[intégration EDF Zen Flex](https://github.com/AuroreVgn/edf-zen-flex).**
> Ce dépôt séparé n'est plus destiné à recevoir de nouvelles versions de la carte. Il est conservé pour l'historique du projet, les anciennes versions et les captures d'écran.
>
> **Attention :** vérifiez qu'une version de l'intégration incluant la carte a bien été publiée avant de désinstaller l'ancienne carte indépendante.

## Installer la carte

Installez ou mettez à jour **[AuroreVgn/edf-zen-flex](https://github.com/AuroreVgn/edf-zen-flex)** via HACS / Marketplace ou manuellement, puis redémarrez Home Assistant.

La ressource JavaScript est fournie par l'intégration :

```text
/edf_zen_flex/zen-flex-card.js
```

L'intégration tente de l'enregistrer automatiquement. Si nécessaire, ajoutez-la dans **Paramètres → Tableaux de bord → Ressources** en tant que **Module JavaScript**.

Ajoutez ensuite une carte manuelle :

```yaml
type: custom:zen-flex-card
title: EDF Zen Flex
mode: full
show_tariffs: true
show_remaining: true
```

La carte conserve ses modes **complet** et **compact**, son calendrier mensuel, les journées Éco / Sobriété / Bonus, les tarifs HP/HC et son éditeur graphique.

## Migration depuis l'installation séparée

1. Installez une version publiée de l'intégration **EDF Zen Flex** qui inclut la carte.
2. Vérifiez que la nouvelle ressource `/edf_zen_flex/zen-flex-card.js` est accessible et enregistrée dans Lovelace.
3. Désinstallez l'ancienne carte `edf-zen-flex_card` installée séparément via HACS, si elle existe.
4. Supprimez uniquement son ancienne ressource JavaScript (par exemple `/hacsfiles/edf-zen-flex_card/zen-flex-card.js` ou `/local/zen-flex-card.js`), **pas** `/edf_zen_flex/zen-flex-card.js`.
5. Actualisez le navigateur. Vos configurations `type: custom:zen-flex-card` restent valides.

Ne chargez pas simultanément les anciennes et nouvelles ressources : elles déclarent le même type de carte.

## Documentation et support

- [README complet, configuration et dépannage](https://github.com/AuroreVgn/edf-zen-flex#readme)
- [Signaler un problème](https://github.com/AuroreVgn/edf-zen-flex/issues)
- [Captures d'écran historiques](assets/)

Merci aux utilisateurs et contributeurs d'EDF Zen Flex Card !
