---
title: Zobrazení historie verzí pro vrácení stránek a fragmentů
description: Tento článek popisuje, jak zobrazit historii verzí pro stránku nebo fragment a vrátit se ke starší verzi v konfigurátoru webů Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 06/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c4d78103a3c08ee4052290fccf6750aba7eecf4a
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474092"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>Zobrazení historie verzí pro vrácení stránek a fragmentů

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak zobrazit historii verzí pro stránku nebo fragment a vrátit se ke starší verzi v konfigurátoru webů Microsoft Dynamics 365 Commerce.

Konfigurátor webů Commerce vám umožňuje zobrazit historii verzí stránky nebo fragmentu a v případě potřeby se vrátit ke konkrétní předchozí verzi dokumentu. Když je dokument otevřený, můžete vybrat **Zobrazit historii** na panelu příkazů a otevřít dialogové okno **Historie verzí**, kde je na kartě **Verze** historie všech verzí a ukládání aktivit pro stránku nebo fragment. Poté můžete v seznamu vybrat předchozí verzi dokumentu, zobrazit její náhled a obnovit ji jako aktuální verzi. Na kartě **Aktivita** dialogového okna je uvedena úplná historie aktivit dokumentu, včetně všech událostí uložení, publikování a zrušení publikování.

> [!NOTE]
> Nová verze dokumentu se vytvoří pokaždé, když autor webu provede změny a poté je vybere **Úpravy dokončeny** pro dokument. 

Chcete-li zobrazit historii verzí pro stránku nebo fragment a vrátit se k předchozí verzi, postupujte takto.

1. V nástroji pro tvorbu webu otevřete stránku nebo fragment, pro který chcete zobrazit historii verzí.
1. Na příkazovém řádku vyberte možnost **Zobrazit historii**.

    ![Tlačítko Zobrazit historii.](./media/version-history-1.png)

1. V dialogovém okně **Historie verzí** na kartě **Verze** vyberte předchozí verzi dokumentu. V podokně vlastností vpravo se zobrazuje miniaturní náhled vybrané verze a informace o tom, kdo a kdy ji upravil.

    ![Zobrazení seznamu historie verzí.](./media/version-history-2.png)

1. Chcete-li zobrazit plně vykreslený náhled vybrané verze dokumentu, vyberte **Náhled**. Chcete-li zavřít náhled a vrátit se do dialogového okna **Historie verzí**, vyberte **Ukončit náhled**.
1. Chcete-li obnovit předchozí verzi dokumentu, vyberte ji v seznamu na kartě **Verze** a poté vyberte **Obnovit**. Zobrazí se okno **Obnovit verzi \<version number\>** a vyzve vás k potvrzení akce obnovení. 

    ![Tlačítko Obnovit a potvrzovací zpráva.](./media/version-history-3.png)

1. Chcete-li pokračovat v akci obnovení, vyberte **Obnovit**. Konfigurátor webu se obnoví a zobrazí obnovenou verzi stránky nebo fragmentu.
1. Chcete-li publikovat obnovenou verzi, vyberte možnost **Dokončit úpravy** a pak vyberte **Publikovat**.
