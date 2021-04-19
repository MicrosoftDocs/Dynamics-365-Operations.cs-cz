---
title: Náhled a publikování experimentu
description: Toto téma popisuje, jak zobrazit náhled a publikovat experiment z Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 52ca23e5aaeb7058853fed2241d5804180fa7f8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798956"
---
# <a name="preview-and-publish-an-experiment"></a>Náhled a publikování experimentu

Toto téma popisuje, jak můžete zobrazit náhled a publikovat experiment v Dynamics 365 Commerce poté, co jste [připojili experiment a upravili varianty](experimentation-connect-edit.md). Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce. Další kroky jsou popsány v samostatných tématech.

[ ![Cesta uživatele experimentováním – náhled a publikování](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Náhled variant experimentu
Můžete si prohlédnout náhled svých variant a dál je upravovat, dokud nebudou vypadat tak, jak chcete.

Chcete-li zobrazit náhled variací experimentu v nástroji pro tvorbu obchodních webů, postupujte takto.

1. V rozevírací nabídce variant pod panelem příkazů obsah, jehož náhled chcete zobrazit. 
1. Na příkazovém řádku vyberte možnost **Náhled**. Zobrazí se náhled, jak bude obsah po publikování vypadat.
1. Když budete chtít zobrazit jinou variantu, vyberte ji z rozevíracího seznamu variant a pak znovu vyberte **Náhled**.

## <a name="publish-your-experiment"></a>Publikování experimentu
Pokud k publikování experimentů na živý web nepoužíváte skupinu publikování a chcete experiment publikovat okamžitě, vyberte **Publikovat** na panelu příkazů. Budou publikovány všechny varianty, které patří k danému experimentu.
    
> [!IMPORTANT]
> Pokud má stránka nepublikovanou adresu URL, musíte nejprve publikovat adresu URL, jinak nebude pro uživatele vašeho webu viditelná. Podrobnosti najdete v tématu [Uložení, náhled a publikování stránky](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Naplánování publikování experimentu na živý web pomocí skupin publikování
Publikování variant vytvořených v konfigurátoru webů můžete naplánovat pomocí skupiny publikování. V rámci skupiny pro publikování můžete k experimentu připojit stránku nebo fragment výběrem **Experimenty** v levém navigačním podokně. Můžete to také provést výběrem **Stránky** nebo **Fragmenty** a podle pokynů v [Připojte experiment a upravte varianty](experimentation-connect-edit.md). Informace o skupinách publikování najdete v tématu [Práce se skupinami publikování](publish-groups.md).

Při používání skupin publikování s experimenty je třeba brát v úvahu několik důležitých aspektů.
- Když do skupiny publikování přidáte stránku nebo fragment se spuštěným experimentem, bude ve skupině publikování tento experiment ze stránky nebo fragmentu odebrán.
- Experimenty, které jsou připojeny ke stránkám na živém webu, nejsou dostupné pro stránky ve skupinách publikování a naopak. Podobně platí, že stránky, na kterých jsou spuštěné experimenty na živém webu, nejsou dostupné jiným experimentům ve skupinách publikování a naopak.
- Při publikování nebo při plánování skupiny publikování je publikován veškerý obsah ve skupině publikování bez ohledu na to, jestli je k této skupině publikování přidružený nějaký experiment.
- Protože skupina publikování přetrvává i poté, co byla publikována na živém webu, experimenty ve skupině pro publikování přetrvávají také. Proto nebudete moct přidružit další experimenty ke stejné stránce nebo fragmentu. Chcete-li se tomuto omezení vyhnout, odstraňte všechny skupiny pro publikování s přetrvávajícími experimenty. Podobně, pokud chcete odstranit experiment na živém webu, který existuje také ve skupině publikování, nejprve ho ze skupiny publikování odstraňte.

## <a name="previous-step"></a>Předchozí krok
[Připojení a úpravy experimentu](experimentation-connect-edit.md)

## <a name="next-step"></a>Další krok
[Spuštění a monitorování experimentu](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]