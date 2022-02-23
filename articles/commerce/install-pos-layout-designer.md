---
title: Instalace návrháře rozložení POS
description: Můžete použít předdefinovaného návrháře k navržení jiných rozložení Modern POS (MPOS) a Cloud POS v režimu rozložení šířku nebo výšku, pro obchody, registrační pokladny, pokladníky a manažery.
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9882ae895de926e0da3579ab65a988f2b97f7be
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410772"
---
# <a name="install-the-pos-layout-designer"></a>Instalace návrháře rozložení POS

[!include [banner](includes/banner.md)]

Můžete použít předdefinovaného návrháře k navržení jiných rozložení Modern POS (MPOS) a Cloud POS v režimu rozložení šířku nebo výšku, pro obchody, registrační pokladny, pokladníky a manažery.

Rozložení grafického návrhu pro MPOS nebo Cloud POS řídí rozložení pokladní zásuvky. Rozložení řídí pozice různých objektů. Mezi příklady patří celkové rozložení, rozložení mřížky položek, rozložení zákazníka, rozložení plateb a rozložení různých tlačítek nabídky. Rozložení zahrnuje také celkový vzhled rozhraní prodeje, které je zaměstnancům předloženo.

## <a name="install-the-one-click-designer"></a>Instalace předdefinovaného návrháře

1. V aplikaci Commerce přejděte z nabídky vlevo nahoře na položky **Maloobchod a velkoobchod** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Rozložení obrazovky**.
2. Vyberte jakékoli rozložení, které má typ aplikace **Moderní POS pro Windows** nebo **Cloud POS**, a klepněte na tlačítko **Návrhář rozložení**.
3. Na panelu oznámení, který se zobrazí v dolní části okna Internet Explorer, klepněte na tlačítko **Otevřít** a spusťte tak instalaci předdefinovaného návrháře. (Panel oznámení se v jiných prohlížečích může zobrazit v různých umístěních.)
4. V poli se zprávou **Aplikace spuštěna - upozornění zabezpečení**, které se zobrazí, klikněte na tlačítko **Spustit** k instalaci hostitele maloobchodního návrháře. Indikátor průběhu zobrazí průběh instalace.
5. Po dokončení instalace zadejte na stránce **Přihlásit** své uživatelské jméno a heslo aplikace Commerce a klikněte na tlačítko **Přihlásit** pro spuštění návrháře.
6. Po ověření pověření a spuštění návrháře můžete začít navrhovat vlastní rozložení nebo změnit existující rozložení.

    [![Rozložení předdefinovaného návrháře](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Poradce při potížích s instalací Návrháře rozložení

- Po klepnutí na tlačítko **Návrhář** se nezobrazí výzva ke stažení (nebo spuštění) instalačního programu nebo vaše stávající nastavení zabezpečení neumožňuje stažení souboru. 

    **Řešení:**

    - V prohlížeči Internet Explorer se ujistěte, že je pro tento web blokování zakázáno. Klepněte na **Nastavení** &gt; **Možnosti** &gt; **Ochrana osobních údajů** &gt; **Najít blokování automaticky otevíraných oken** a změňte nastavení, pokud je požadována změna.
    - V prohlížeči Internet Explorer přidejte URL adresu Commerce do svých důvěryhodných webů. Klikněte na **Nastavení** &gt; **Možnosti** &gt; **Zabezpečení** &gt; **Důvěryhodné weby** &gt; **Weby** &gt; **Přidat**.

- Program nelze spustit, a jste vyzváni, abyste kontaktovali dodavatele.

    **Řešení:** V prohlížeči Internet Explorer přidejte adresu URL Commerce do svých důvěryhodných webů. Klikněte na **Nastavení** &gt; **Možnosti** &gt; **Zabezpečení** &gt; **Důvěryhodné weby** &gt; **Weby** &gt; **Přidat**.

**Známý problém**: návrhář správně nefunguje v prohlížečích Google Chrome a Mozilla Firefox. Na opravě tohoto problému pracujeme.

## <a name="additional-resources"></a>Další prostředky

[Konfigurace, Instalace a aktivace Retail Modern POS (MPOS)](retail-modern-pos-device-activation.md)
