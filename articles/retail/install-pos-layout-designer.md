---
title: "Instalace návrháře rozložení Retail POS"
description: "Můžete použít předdefinovaného návrháře k navržení jiných rozložení Retail Modern POS (MPOS) a Cloud POS v režimu rozložení šířku nebo výšku, pro obchody, registrační pokladny, pokladníky a manažery."
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8fdebf692bd3cd8500274cc73ca5b0591dba4140
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="install-the-retail-pos-layout-designer"></a>Instalace návrháře rozložení Retail POS

[!include[banner](includes/banner.md)]


Můžete použít předdefinovaného návrháře k navržení jiných rozložení Retail Modern POS (MPOS) a Cloud POS v režimu rozložení šířku nebo výšku, pro obchody, registrační pokladny, pokladníky a manažery.

Rozložení grafického návrhu pro MPOS nebo Cloud POS řídí rozložení pokladní zásuvky. Rozložení řídí pozice různých objektů. Mezi příklady patří celkové rozložení, rozložení mřížky položek, rozložení zákazníka, rozložení plateb a rozložení různých tlačítek nabídky. Rozložení zahrnuje také celkový vzhled rozhraní prodeje, které je zaměstnancům předloženo.

## <a name="install-the-one-click-designer"></a>Instalace předdefinovaného návrháře
1.  V aplikaci Microsoft Dynamics 365 for Retail přejděte v nabídce vlevo nahoře na položky **Maloobchodní** **a velkoobchodní prodej** &gt; **Instalace kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Rozložení obrazovky**.
2.  Vyberte jakékoli rozložení, které má typ aplikace **Moderní POS pro Windows** nebo **Cloud POS**, a klepněte na tlačítko **Návrhář rozložení**.
3.  Na panelu oznámení, který se zobrazí v dolní části okna Internet Explorer, klepněte na tlačítko **Otevřít** a spusťte tak instalaci předdefinovaného návrháře. (Panel oznámení se v jiných prohlížečích může zobrazit v různých umístěních.)
4.  V poli se zprávou **Aplikace spuštěna - upozornění zabezpečení**, které se zobrazí, klikněte na tlačítko **Spustit** k instalaci hostitele maloobchodního návrháře. Indikátor průběhu zobrazí průběh instalace.
5.  Po dokončení instalace na stránce **Přihlásit** zadejte uživatelské jméno a heslo pro aplikaci Microsoft Dynamics 365 for Retail a kliknutím na tlačítko **Přihlásit se** spusťte modul návrháře.
6.  Po ověření pověření a spuštění návrháře můžete začít navrhovat vlastní rozložení nebo změnit existující rozložení. [![Rozložení předdefinovaného návrháře](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Poradce při potížích s instalací Návrháře rozložení
-   Po klepnutí na tlačítko **Návrhář** se nezobrazí výzva ke stažení (nebo spuštění) instalačního programu nebo vaše stávající nastavení zabezpečení neumožňuje stažení souboru. **Řešení:**
    -   V aplikaci Internet Explorer se ujistěte, že je pro tento web blokování zakázáno. Klepněte na **Nastavení** &gt; **Možnosti** &gt; **Ochrana osobních údajů** &gt; **Najít blokování automaticky otevíraných oken** a změňte nastavení, pokud je požadována změna.
    -   V aplikaci Internet Explorer přidejte adresu URL aplikace Dynamics 365 for Retail do seznamu důvěryhodných webů. Klikněte na **Nastavení** &gt; **Možnosti** &gt; **Zabezpečení** &gt; **Důvěryhodné weby** &gt; **Weby** &gt; **Přidat**.
-   Program nelze spustit, a jste vyzváni, abyste kontaktovali dodavatele. **Řešení:** V aplikaci Internet Explorer přidejte adresu URL aplikace Dynamics 365 for Retail do seznamu důvěryhodných webů. Klikněte na **Nastavení** &gt; **Možnosti** &gt; **Zabezpečení** &gt; **Důvěryhodné weby** &gt; **Weby** &gt; **Přidat**.

**Známý problém:** návrhář správně nefunguje v prohlížečích Google Chrome a Mozilla Firefox. Na opravě tohoto problému pracujeme.

<a name="see-also"></a>Viz také
--------

[Konfigurace, stažení, instalace a aktivace Retail Modern POS](retail-modern-pos-device-activation.md)




