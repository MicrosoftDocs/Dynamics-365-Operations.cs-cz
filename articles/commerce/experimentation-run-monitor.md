---
title: Spuštění a monitorování experimentu
description: Toto téma popisuje, jak spustit a monitorovat experiment ve službě třetí strany. Popisuje také, jak můžete provádět změny variant po spuštění experimentu.
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
ms.openlocfilehash: 4afc19ed103f204fec61ab20b88f767ad5f05b38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792528"
---
# <a name="run-and-monitor-an-experiment"></a>Spuštění a monitorování experimentu

Toto téma popisuje, jak můžete spustit a monitorovat experiment v aplikaci třetí strany a jak můžete v případě potřeby měnit varianty. Než provedete kroky v tomto tématu, budete nejprve muset [publikovat](experimentation-preview-publish.md) váš experiment v Commerce. 

Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce. Další kroky jsou popsány v samostatných tématech.

[ ![Cesta uživatele experimentováním – spuštění a monitorování](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Jakmile své varianty publikujete, jsou provedeny všechny kroky, které musíte provést v Commerce, abyste mohli experiment spustit. Dalším krokem je určení, která varianta se má zobrazit jednotlivým uživatelům, když budou požadovat zobrazení stránky. Toto rozhodnutí dělá služba třetí strany, ale nejprve musíte v této službě experiment aktivovat. Vzhledem k tomu, že kroky pro aktivaci experimentu se u jednotlivých služeb liší, budete muset postupovat podle pokynů vaší služby nebo poskytovatele. Pokud experiment není aktivován, uvidí uživatelé pouze výchozí verzi stránky (nezobrazí se žádné varianty).

Experiment budete muset nechat běžet dostatečně dlouho, aby se shromáždila data pro statisticky platné výsledky. Pomocí služby třetí strany můžete během experimentu monitorovat data experimentu a analýzu.

## <a name="adjust-your-variations"></a>Úprava variant
Pokud budete z nějakého důvodu potřebovat své varianty upravit, postupujte podle pokynů níže.

> [!IMPORTANT]
> Pokud provedete změny v živém experimentu v Commerce nebo ve službě třetí strany, může to významně ovlivnit výsledky. V případě zásadních změn zvažte, jestli není lepší nechat experiment proběhnout a pak vytvořit nový experiment.

1. V konfigurátoru webů Commerce vyberte **Experimenty** v levém navigačním podokně a poté vyberte experiment. 
1. V rozevírací nabídce vyberte variantu, kterou chcete aktualizovat.
1. Proveďte libovolné potřebné změny, pak zobrazte náhled a varianty publikujte. Další informace najdete v tématu [Náhled a publikování experimentu](experimentation-preview-publish.md).
1. Přejděte do služby třetí strany a proveďte všechny změny související s nastavením experimentu.
    
## <a name="previous-step"></a>Předchozí krok
[Náhled a publikování experimentu](experimentation-preview-publish.md)

## <a name="next-step"></a>Další krok
[Povýšení varianty a dokončení experimentu](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]