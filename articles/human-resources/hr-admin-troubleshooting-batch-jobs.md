---
title: Optimalizace výkonu plánováním dávkových úloh po pracovní době
description: V tomto článku se vysvětluje, jak řešit některé problémy s aplikací Microsoft Dynamics 365 Human Resources plánováním dlouho běžících dávkových úloh po pracovní době.
author: twheeloc
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6efb0a906bb948a47f03665dd6e7a8dd43434083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896069"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Optimalizace výkonu plánováním dávkových úloh po pracovní době


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>Výdej

Pokud jsou dávkové úlohy, jež běží dlouho, spouštěny během běžné pracovní doby, může mít Microsoft Dynamics 365 Human Resources problémy s výkonem.

## <a name="resolution"></a>Rozlišení

Následující dávkové úlohy plánujte na dobu po pracovní době. Doporučujeme také přezkoumat frekvenci dávkových úloh, které se spouští často. Pokud je to možné, snižte frekvenci opakování dávkové úlohy. V mnoha případech je dostatečná výchozí frekvence.

Následující dávkové úlohy by měly být spouštěny v noci nebo po pracovní době. U těchto opakujících se dávkových úloh zkontrolujte časové pásmo. Některé dávkové úlohy mohou používat tichomořský standardní čas (PST).

| Dávková úloha | Výchozí výskyt |
| --- | --- |
| Vymazání historie dávkových úloh | 1krát za měsíc |
| Exportovat vyčištění fázování | 1krát denně |
| Synchronizace zmeškaného požadavku integrace Common Data Service | 1krát denně |
| Systémová úloha komprese databáze, jež musí běžet pravidelně mimo pracovní dobu | 1krát denně |
| Systémová úloha sestavení nového indexu databáze, jež musí běžet pravidelně mimo pracovní dobu | 1krát denně |

1. V modulu Human Resources vyberte **Správa systému**.

2. Pomocí **vyhledávací** lišty vyhledejte jednu z výše uvedených dávkových úloh.

3. Vyberte možnost **Spustit na pozadí** a vyberte **Opakování**.

   ![Nastavení opakování.](media/talent-batch-history-cleanup-recurrence.png)

4. V části **Definovat opakování** nastavte **Počáteční datum** a **Počáteční čas** mimo pracovní dobu nebo víkend. Vyberte **Bez koncového data**. 

   ![Definování počátečního data a času opakování.](media/talent-batch-history-cleanup-define-recurrence.png)

5. Vyberte **OK**.

6. V případě potřeby změňte všechny ostatní parametry v podnabídce **Spustit na pozadí** a pak vyberte **OK**.

## <a name="additional-resources"></a>Další prostředky

[Optimalizace výkonu pomocí úloh automatického vyčištění](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
