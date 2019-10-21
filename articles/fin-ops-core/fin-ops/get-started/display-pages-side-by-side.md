---
title: Zobrazení stránek vedle sebe pomocí funkce Otevřít v novém okně
description: Tento článek vysvětluje způsob zobrazení stránek vedle sebe.
author: aneesmsft
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7144f26c0977fbc420b804728151262b2f166bc0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180684"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a>Zobrazení stránek vedle sebe pomocí funkce Otevřít v novém okně

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje způsob zobrazení stránek vedle sebe.

Můžete zobrazit více stránek souběžně a rychle tak dokončit úlohu. Například můžete ověřit nebo zadat řádky do více než jednoho deníku. Obvykle je třeba přejít oběma směry mezi stránkou, která zobrazuje seznam deníků, a stránkou, která zobrazuje řádky daného deníku. Funkce **Otevřít v novém okně** umožňuje zobrazení těchto stránek souběžně, aby bylo možné provést úlohy rychle.

V souladu s příkladem uvedeným výše lze při prohlížení řádků kliknout na ikonu **Otevřít v novém okně**.

[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Kliknutím na ikonu **Otevřít v novém okně** otevře stránku s řádky v novém místním prohlížeči a poté přejde v původním prohlížeči v historii na stránku zobrazující seznam deníků. Pak můžete zobrazit obě stránky souběžně. Po dokončení zobrazení deníku můžete změnit vybraný deník na stránce seznamu deníků a stránku s řádky v místním okně automaticky zobrazí řádky nově vybraného deníku.

[![stránky-se-zobrazí-vedle-sebe](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Dynamické propojení a aktualizace probíhá kvůli vztahům, které existují mezi daty, která podporují tyto stránky. Pokud systém není obeznámen se vztahy mezi daty, místní okno se nebude automaticky aktualizovat po změně původního okna.

Některé stránky obsahují více zobrazení, jako je například zobrazení mřížky, zobrazení záhlaví a zobrazení podrobností. Ikona **Otevřít v novém okně** způsobí, že celá stránka bude otevřena v novém okně prohlížeče. Proto nelze ponechat dvě zobrazení stejné stránky vedle sebe pomocí funkce **Otevřít v novém okně**. Téměř všechny tyto stránky však mají navigační seznam, pomocí kterého můžete přepínat mezi záznamy a dosáhnout tak podobné zkušenosti.

Před použitím funkce **Otevřít v novém okně** je třeba nakonfigurovat funkci blokování automaticky otevíraných oken prohlížeče tak, aby umožnila otevírání automaticky otevíraných oken z adresy URL serveru. Například je možné povolit automatické otevírání oken z adresy "\*.dynamics.com".

Funkce **Otevřít v novém okně** je k dispozici pouze, pokud existuje více než jedna stránka otevřená v okně. Dále se místní okno automaticky zavře, pokud nejsou žádné další stránky otevřeny (tj. když je zavřena poslední stránka v tomto okně). Systém také zavře otevřené stránky, když přejdete do jiné oblasti aplikace. Z toho vyplývá, že pokud máte otevřená místní okna a přejdete do jiné oblasti v aplikaci, místní okna budou automaticky uzavřena, protože stránky v těchto oknech byly zavřeny systémem.

Horní panel v místních oknech zobrazuje informace o společnosti, ve které byla stránka otevřena a je určena jen ke čtení. Místní podokna jsou závislá na hlavním okně prohlížeče. Je-li hlavní okno zavřeno nebo aktualizováno, všechna otevřená místní okna se stanou jen pro čtení. To znamená, že stále můžete prohlížet údaje v těchto oknech, ale nebudete moci s nimi spolupracovat.
