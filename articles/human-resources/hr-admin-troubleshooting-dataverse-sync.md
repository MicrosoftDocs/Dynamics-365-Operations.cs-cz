---
title: Resetování synchronizace Dataverse
description: Toto téma popisuje řešení potíží se záznamy, které se nesynchronizují správně mezi aplikací Microsoft Dynamics 365 Human Resources a řešením správy lidského kapitálu HCM Common v Microsoft Dataverse.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d6b20b6b2ae4fdbbfb27a765dfb7a1dc82fe7981
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071153"
---
# <a name="reset-dataverse-synchronization"></a>Resetování synchronizace Dataverse


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Problém

Záznamy nejsou synchronizovány mezi aplikací Microsoft Dynamics 365 Human Resources a entitami v řešení správy lidského kapitálu HCM Common v Microsoft Dataverse. Další informace o synchronizaci najdete v tématu [Konfigurace integrace Dataverse](hr-admin-integration-common-data-service.md). Nesprávná synchronizace může nastat, když se **integrace Dataverse opakuje** nebo když dávkové úlohy **synchronizace zmeškaného požadavku integrace Dataverse** uvízly ve stavu **Zpracování**.

## <a name="resolution"></a>Řešení

Když se **integrace Dataverse opakuje** nebo když **dávkové úlohy synchronizace zmeškaného požadavku integrace Dataverse** uvízly ve stavu **Zpracování** nebo **Ruší se**, můžete stav resetovat. To lze provést zrušením dávkové úlohy podle pokynů v části [Reset zablokovaných dávkových úloh](hr-admin-troubleshooting-batch-execution.md). Po zrušení dávkové úlohy ji můžete resetovat nastavením do stavu **Čekání**. Dávková úloha se pak spustí během dalšího naplánovaného běhu.

1. Pokud jste tak ještě neučinili, povolte funkci **Vylepšené přerušení dávky** ve **Správě funkcí**.
   1. Přejděte na stránku **Správa funkcí** (**Správa systému** > **Souhrn** > **Správa funkcí**).
   2. Vyberte kartu **Vše**.
   3. Vyberte sloupec **Název funkce** a filtrujte ho podle **Vylepšeného přerušení dávky**.
   4. Vyberte akci **Umožnit**, pokud ještě není povolena.

2. Vypněte integraci Dataverse.
   1. Přejděte na stránku **Integrace Microsoft Dataverse** (ve **Správě systému** přejděte na **Odkazy** > **Integrace** > **Konfigurace Dataverse**).
   2. Nastavte možnost **Povolit integraci Dataverse** na **Ne**.

3. Zrušte dávkovou úlohu **Opakovat integraci Dataverse**.
   1. Přejděte na stránku **Dávkové úlohy** (ve **Správě systému** přejděte na **Odkazy** >  **Dávkové úlohy** >  **Dávkové úlohy**).
   2. Filtrujte sloupec **Popis práce** podle **Integrace**.
   3. Vyberte dávkovou úlohu **Opakovat integraci Dataverse**.
   4. Na pásu karet akcí vyberte **Dávková úloha**, **Vynutit zrušení** a poté potvrďte výběrem **Ano**.

   > [!NOTE]
   > V závislosti na tom, kdy byla integrace poprvé povolena, může mít dávková úloha popis **Opakovat integraci Common Data Service**. Vyberte tuto dávkovou úlohu, pokud je uvedena, namísto dávkové úlohy **Opakovat integraci Dataverse**.

4. Odstraňte všechny dávkové úlohy integrace Dataverse.
   1. Na stránce **Dávkové úlohy** vyberte dávkové úlohy **Synchronizace zmeškaného požadavku integrace Dataverse**, **Opakovat integraci Dataverse** a **Počáteční synchronizace integrace Dataverse**.
   2. Na pásu karet akcí vyberte akci **Změnit stav**. 
   3. Vyberte **Srážka** a pak vyberte **OK**.
   4. Na pásu karet akcí vyberte akci **Odstranit** a poté akci potvrďte výběrem **Ano**.

5. Zapněte dávkové úlohy integrace Dataverse.
   1. Přejděte na stránku **Integrace Microsoft Dataverse** (**Správa systému** > **Odkazy** > **Integrace** > **Konfigurace Dataverse**).
   2. Nastavte možnost **Povolit integraci Dataverse** na **Ano**.

6. Přejděte na stránku **Dávkové úlohy** a potvrďte, že byly vytvořeny dávkové úlohy **Opakovat integraci Dataverse** a **Synchronizace zmeškaného požadavku integrace Dataverse**.

Když jsou dávkové úlohy opětovně vytvořeny, můžete sledovat dávkovou úlohu **Opakovat integraci Dataverse**, abyste zjistili, jak dlouho trvá její provedení. Poté můžete ověřit, že se záznamy synchronizují správně s řešením HCM Common v Microsoft Dataverse.

## <a name="see-also"></a>Viz také

[Konfigurace integrace s Dataverse](hr-admin-integration-common-data-service.md)<br>
[Reset zablokovaných dávkových úloh](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
