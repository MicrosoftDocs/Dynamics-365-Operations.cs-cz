---
title: Zobrazení stránek vedle sebe pomocí funkce Otevřít v novém okně
description: Tento článek vysvětluje způsob zobrazení stránek vedle sebe.
author: aneesmsft
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f082fe4af9c095d841dbcabf85d365a3fbee71b79a7765e39fbe691db7da458e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771943"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a>Zobrazení stránek vedle sebe pomocí funkce Otevřít v novém okně

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje způsob zobrazení stránek vedle sebe.

Můžete zobrazit více stránek souběžně a rychle tak dokončit úlohu. Například můžete ověřit nebo zadat řádky do více než jednoho deníku. Obvykle je k ověření nebo zadání řádků do více než jednoho deníku třeba přejít oběma směry mezi stránkou, která zobrazuje seznam deníků, a stránkou, která zobrazuje řádky daného deníku. Funkce **Otevřít v novém okně** umožňuje zobrazení těchto stránek souběžně, aby bylo možné provést úlohy rychle.

V souladu s příkladem uvedeným výše lze při prohlížení řádků kliknout na ikonu **Otevřít v novém okně**.

[![Klikněte na ikonu Otevřít v novém okně.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Kliknutím na ikonu **Otevřít v novém okně** otevře stránku s řádky v novém místním prohlížeči a poté přejde v původním prohlížeči v historii na stránku zobrazující seznam deníků. Pak můžete zobrazit obě stránky souběžně. Po zobrazení deníku můžete změnit vybraný deník na stránce seznamu deníků a stránku s řádky v místním okně automaticky zobrazí řádky nově vybraného deníku.

[![Můžete zobrazit obě stránky souběžně.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Dynamické propojení a aktualizace probíhá kvůli vztahům, které existují mezi daty, která podporují tyto stránky. Pokud systém není obeznámen se vztahy mezi daty, místní okno se nebude automaticky aktualizovat po změně původního okna.

Některé stránky obsahují více zobrazení, jako je například zobrazení mřížky, zobrazení záhlaví a zobrazení podrobností. Ikona **Otevřít v novém okně** způsobí, že celá stránka bude otevřena v novém okně prohlížeče. Proto nelze ponechat dvě zobrazení stejné stránky vedle sebe pomocí funkce **Otevřít v novém okně**. Téměř všechny tyto stránky mají navigační seznam, pomocí kterého můžete přepínat mezi záznamy a dosáhnout tak podobné zkušenosti.

Před použitím funkce **Otevřít v novém okně** je třeba nakonfigurovat funkci blokování automaticky otevíraných oken prohlížeče tak, aby umožnila otevírání automaticky otevíraných oken z adresy URL serveru. Například je možné povolit automatické otevírání oken z adresy "\*.dynamics.com".

Funkce **Otevřít v novém okně** je k dispozici pouze, pokud existuje více než jedna stránka otevřená v okně. Dále se místní okno automaticky zavře, pokud nejsou žádné další stránky otevřeny (tj. když je zavřena poslední stránka v tomto okně). Systém také zavře otevřené stránky, když přejdete do jiné oblasti aplikace. Z toho vyplývá, že pokud máte otevřená místní okna a přejdete do jiné oblasti v aplikaci, místní okna budou automaticky uzavřena, protože stránky v těchto oknech byly zavřeny systémem.

Horní panel v místních oknech zobrazuje informace o společnosti, ve které byla stránka otevřena a je určena jen ke čtení. Místní podokna jsou závislá na hlavním okně prohlížeče. Je-li hlavní okno zavřeno nebo aktualizováno, všechna otevřená místní okna se stanou jen pro čtení. Pokud k tomu dojde, můžete stále prohlížet údaje v těchto oknech, ale nebudete moci s nimi spolupracovat.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]