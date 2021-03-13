---
title: Operace odvolání objednávky v POS
description: Toto téma vysvětluje funkce, které jsou dostupné u vylepšených stránek pro odvolání objednávek v POS.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010067"
---
# <a name="recall-order-operation-in-pos"></a>Operace odvolání objednávky v POS

[!include [banner](includes/banner.md)]

Operace **Odvolat objednávku** v pokladním místě (POS) Commerce nabízí aktualizované funkce hledání a filtrování objednávek a specifické informace o objednávce. Tato funkce je k dispozici ve verzích Commerce 10.0.15 a novějších.

Tuto funkčnost povolíte tak, že zapnete funkci **Vylepšená operace odvolání objednávky v POS** v pracovním prostoru **Správa funkcí** v centrále Commerce. Po povolení této funkce zvažte aktualizaci [rozložení obrazovek](pos-screen-layouts.md) v POS, abyste využili některé ze změněných funkcí.

Konfigurace tlačítka operace **Odvolání objednávky** umožňuje organizacím nasadit tuto operaci s předdefinovaným zobrazením.

![Konfigurace mřížky tlačítek](media/recallorderbuttongrid.png)

K dispozici jsou následující možnosti zobrazení.
- **Žádné** – tato možnost nasadí tuto operaci bez konkrétního zobrazení. Když uživatel otevře operaci s touto konfigurací, bude vyzván k vyhledání objednávek nebo k výběru z předdefinovaného filtru objednávek.
- **Objednávky k plnění** – když uživatel zahájí tuto operaci, automaticky se spustí dotaz, který vyhledá a zobrazí seznam objednávek, které má obchod splnit. Tyto objednávky jsou nakonfigurovány pro výdej v obchodě nebo dodávku z obchodu, přičemž řádky těchto objednávek ještě nebyly vydány nebo zabaleny.
- **Objednávky k vydání** – když uživatel zahájí tuto operaci, automaticky se spustí dotaz, který vyhledá a zobrazí seznam objednávek, které jsou nakonfigurovány pro výdej v aktuálním obchodě uživatele.
- **Objednávky k dodávce** – když uživatel zahájí tuto operaci, automaticky se spustí dotaz, který vyhledá a zobrazí seznam objednávek, které jsou nakonfigurovány pro dodávku z aktuálního obchodu uživatele.

Pokud uživatel zahájí operaci **Odvolat objednávku** z POS, když je zobrazení je nakonfigurováno na **Žádné**, bude moci objednávky vyhledat a načíst jedním z následujících způsobů.
- Naskenuje čárové kódy objednávek. Tím se vyhledají shody s poli pro číslo objednávky, odkaz na kanál a ID účtenky.
- Vybere ikonu **Hledat objednávky** nebo **Hledat a filtrovat** na panelu aplikace a pomocí filtračního mechanizmu vyhledá objednávky, které splňují kritéria filtru.
- Zvolí z předdefinovaného filtru v rozevírací nabídce **Zobrazit objednávky** (objednávky k plnění, objednávky k vydání nebo objednávky k dodávce).

![Hlavní nabídka odvolání objednávky](media/recallordermain.png)

Po uplatnění kritérií hledání zobrazí aplikace seznam odpovídajících prodejních objednávek.

![Podrobnosti odvolání objednávky](media/orderrecalldetail.png)

Výběrem objednávky v seznamu může uživatel zobrazit další podrobnosti. Informační panel na pravé straně obrazovky zobrazuje specifika vybrané objednávky, včetně podrobností o řádku objednávky, doručení a plnění.

Na panelu aplikace může uživatel vybrat některou operaci. V závislosti na stavu objednávky nemusí být některé operace povoleny.

- **Vrátit** – provede vrácení jedné nebo více faktur souvisejících s vybranou objednávkou odběratele.

- **Storno** – vystaví úplné zrušení vybrané prodejní objednávky.

- **Splnit** – přenese uživatele na stránku pro splnění objednávky, která bude předfiltrována na vybranou objednávku. Zobrazí se pouze řádky vybrané objednávky, které jsou otevřené pro splnění obchodem uživatele.

- **Upravit** – umožňuje uživatelům provádět změny ve vybrané objednávce odběratele.

- **Vydat** – spustí tok vydání, který uživateli umožňuje vybrat produkty, které mají být vydány, a vytvoří prodejní transakci výdeje.
