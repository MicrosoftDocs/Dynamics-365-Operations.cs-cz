---
title: "Instalace návrháře rozložení Retail POS"
description: "Můžete použít předdefinovaného návrháře k navržení jiných rozložení Retail Modern POS (MPOS) a Cloud POS v režimu rozložení šířku nebo výšku, pro obchody, registrační pokladny, pokladníky a manažery."
author: MargoC
manager: AnnBe
ms.date: 2016-10-28 19 - 05 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b33cbf67c00b6baea4393e82d19300085781af29
ms.lasthandoff: 03/31/2017


---

# <a name="install-the-retail-pos-layout-designer"></a>Instalace návrháře rozložení Retail POS

Můžete použít předdefinovaného návrháře k navržení jiných rozložení Retail Modern POS (MPOS) a Cloud POS v režimu rozložení šířku nebo výšku, pro obchody, registrační pokladny, pokladníky a manažery.

Rozložení grafického návrhu pro MPOS nebo Cloud POS řídí rozložení pokladní zásuvky. Rozložení řídí pozice různých objektů. Mezi příklady patří celkové rozložení, rozložení mřížky položek, rozložení zákazníka, rozložení plateb a rozložení různých tlačítek nabídky. Rozložení zahrnuje také celkový vzhled rozhraní prodeje, které je zaměstnancům předloženo.

## <a name="install-the-oneclick-designer"></a>Instalace předdefinovaného návrháře
1.  V aplikaci Microsoft Dynamics 365 for Operations přejděte z nabídky vlevo nahoře na položky **Maloobchodní** **velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Rozložení obrazovky**.
2.  Vyberte jakékoli rozložení, které má typ aplikace **Moderní POS pro Windows** nebo **Cloud POS**, a klepněte na tlačítko **Návrhář rozložení**.
3.  Na panelu oznámení, který se zobrazí v dolní části okna Internet Explorer, klepněte na tlačítko **Otevřít** a spusťte tak instalaci předdefinovaného návrháře. (Panel oznámení se v jiných prohlížečích může zobrazit v různých umístěních.)
4.  V poli se zprávou **Aplikace spuštěna - upozornění zabezpečení**, které se zobrazí, klikněte na tlačítko **Spustit **k instalaci hostitele maloobchodního návrháře. Indikátor průběhu zobrazí průběh instalace.
5.  Po dokončení instalace na stránce **Přihlásit** zadejte uživatelské jméno a heslo aplikace Microsoft Dynamics 365 for Operations a klepněte na tlačítko **Přihlásit** ke spuštění návrháře.
6.  Po ověření pověření a spuštění návrháře můžete začít navrhovat vlastní rozložení nebo změnit existující rozložení. [![Rozložení předdefinovaného návrháře](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Poradce při potížích s instalací Návrháře rozložení
-   Po klepnutí na tlačítko **Návrhář** se nezobrazí výzva ke stažení (nebo spuštění) instalačního programu nebo vaše stávající nastavení zabezpečení neumožňuje stažení souboru. **Řešení:**
    -   V aplikaci Internet Explorer se ujistěte, že je pro tento web blokování zakázáno. Klepněte na **Nastavení** &gt; **Možnosti** &gt; **Ochrana osobních údajů** &gt; **Najít blokování automaticky otevíraných oken** a změňte nastavení, pokud je požadována změna.
    -   V aplikaci Internet Explorer přidejte adresu URL Dynamics 365 for Operations do seznamu důvěryhodných webů. Klikněte na **Nastavení** &gt; **Možnosti** &gt; **Zabezpečení** &gt; **Důvěryhodné weby** &gt; **Weby** &gt; **Přidat**.
-   Program nelze spustit, a jste vyzváni, abyste kontaktovali dodavatele. **Řešení:** V aplikaci Internet Explorer přidejte adresu URL Dynamics 365 for Operations do seznamu důvěryhodných webů. Klikněte na **Nastavení** &gt; **Možnosti** &gt; **Zabezpečení** &gt; **Důvěryhodné weby** &gt; **Weby** &gt; **Přidat**.

**Známý problém:** návrhář správně nefunguje v prohlížečích Google Chrome a Mozilla Firefox. Na opravě tohoto problému pracujeme.

<a name="see-also"></a>Viz také
--------

[Konfigurace, stažení, instalace a aktivace Retail Modern POS](retail-modern-pos-device-activation.md)


