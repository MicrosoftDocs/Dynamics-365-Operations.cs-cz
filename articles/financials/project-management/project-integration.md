---
title: "Klientská integrace aplikace Microsoft Project"
description: "Plánování a údržba plánu projektu může být složitá. Projektoví manažeři proto potřebují používat nástroje, které jim pomohou spravovat tento úkol. Integrace s klientem Microsoft Project poskytuje podporu pro otevření a správu strukturovaného rozpisu prací na projektu."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a3445417d5ae88e2ff3676962a82921a7ab475d
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="microsoft-project-client-integration"></a>Klientská integrace aplikace Microsoft Project

[!include [banner](../includes/banner.md)]

Plánování a údržba plánu projektu může být složitá. Projektoví manažeři proto potřebují používat nástroje, které jim pomohou spravovat tento úkol. Integrace s klientem Microsoft Project poskytuje podporu pro otevření a správu strukturovaného rozpisu prací na projektu. Projektový manažer může publikovat jakékoliv změny zpět do strukturovaného rozpisu prací na projektu aplikace Finance and Operations.

> [!NOTE]
> Pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations v aktualizaci z července 2017, musíte si nainstalovat KB 4054797 a 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurace doplňku klienta Microsoft Project
Chcete-li povolit integraci s klientem Microsoft Project, musí být nainstalován doplněk Microsoft Dynamics 365 v klientovi uživatele aplikace Microsoft Project. Otevřete **Pracovní prostor Správa projektu**.

•   Klikněte na tlačítko **Konfigurace doplňku klienta Microsoft Project** z části pracovního prostoru **Odkazy** > **Nastavení**.

•   Klikněte na **Otevřít**, poté klikněte po zobrazení výzvy na **Spustit**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Otevření a úprava stávajícího konceptu strukturovaného rozpisu prací v klientovi Microsoft Project
Pokud má projekt již v aplikaci Finance and Operation vytvořený strukturovaný rozpis prací, lze ho otevřít v aplikaci klienta Microsoft Project, pokud je strukturovaný rozpis prací ve stavu konceptu. Chcete-li ho otevřít ze stránky **Projekt**, klikněte na odkaz **Otevřít v aplikaci Microsoft Project** z karty **Plán**. Tuto stránku lze rovněž otevřít z aplikace klienta Microsoft Project kliknutím na **Otevřít** na kartě **Microsoft Dynamics 365**. Zvolte **Právnická osoba** a **Projekt** ze seznamu.

> [!NOTE]
> Používáte-li jako prohlížeč Internet Explorer, musíte kliknout na tlačítko **Uložit** pro ruční otevření z umístění, do kterého je soubor stažený. Klikněte na tlačítko **Uložit a otevřít** a otevřete soubor v klientovi Microsoft Project. Při ukládání neměňte název souboru.

Před provedením jakýchkoliv úprav souboru pomocí klienta aplikace Microsoft Project je třeba ho nejprve rezervovat. Klikněte na tlačítko **Rezervovat** na kartě **Microsoft Dynamics 365**. Ostatním uživatelům zabráníte v souběžných úpravách strukturovaného rozpisu prací aplikace Finance and Operations. Chcete-li publikovat strukturovaný rozpis prací po dokončení úprav, klikněte na tlačítko **Vrátit se změnami** na kartě **Microsoft Dynamics 365**.

Je-li projektový tým již přidán do projektu Finance and Operations, seznam zdrojů bude vyplněn členy týmu. Není-li tým ještě přidán do projektu, můžete vybrat zdroje a vytvořit tým v klientovi Microsoft Project klikinutím na tlačítko **Zdroje** na kartě **Microsoft Dynamics 365**. 

Následující data budou synchronizována zpět do aplikace Finance and Operation jako součást procesu vrácení se změnami:

•   Název úkolu

•   Počáteční datum

•   Datum dokončení

•   Předchůdci

•   Názvy zdrojů

•   Kategorie

•   Kategorie prostředků

•   Pracovní hodiny

•   Poznámky

•   Priorita

> [!NOTE]
> Pokud přidáte další sloupce do souboru klienta aplikace Microsoft Project, nebudou uloženy do souboru a nezobrazí se při opakovaném otevření souboru.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Vytvoření strukturovaného rozpisu prací pro existující projekt pomocí klienta aplikace Microsoft Project
Pro vytvoření nového strukturovaného rozpisu prací pomocí klienta Microsoft Project postupujte podle těchto kroků:


1.  Otevřete klienta Microsoft Project.

2.  Na kartě **Microsoft Dynamics 365** klikněte na **Otevřít**.

3.  Vyberte **Právnická osoba** pro projekt.

4.  Vyberte **Projekt**.

5.  Klikněte na **Rezervovat** na kartě **Microsoft Dynamics 365**.

6.  Až budete připraveni publikovat do Finance and Operations, klikněte na **Vrátit se změnami** na kartě **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Nahrazení stávajícího strukturovaného rozpisu prací pro existující projekt pomocí klienta aplikace Microsoft Project
Chcete-li vytvořit nový strukturovaný rozpis prací pomocí klienta Microsoft Project a nahradit existující strukturovaný rozpis prací pro existující projekt, postupujte takto:

1.  Otevřete klienta Microsoft Project.

2.  Vytvořte plán v klientovi Microsoft Project

3.  Na kartě **Microsoft Dynamics 365** klikněte na **Uložit změny** > **Nahradit stávající projekt**.

4.  Vyberte **Právnická osoba** pro projekt.

5.  Vyberte **Projekt**.

6.  Klikněte na tlačítko **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Vytvoření nového projektu z klienta Microsoft Project


1.  Otevřete klienta Microsoft Project.

2.  Vytvořte plán v klientovi Microsoft Project

3.  Na kartě **Microsoft Dynamics 365** klikněte na **Uložit změny** > **Uložit do nového projektu**.

4.  Vyberte **Právnická osoba** pro projekt.

5.  Zadejte **ID projektu**, pokud je to nutné.

6.  Zadejte **Název projektu**.

7.  Vyberte **Typ projektu**, **Skupina projektu** a **ID smlouvy projektu**. Také můžete vytvořit novou projektovou smlouvu kliknutím na **Nová**.

8.  Vyberte **Kalendář**, který se použije pro zdroje.

11. Klikněte na tlačítko **OK**.

