---
title: Optimalizace výkonu plánováním dávkových úloh po pracovní době
description: V tomto tématu se vysvětluje, jak řešit některé problémy s aplikací Microsoft Dynamics 365 Human Resources plánováním dlouho běžících dávkových úloh po pracovní době.
author: andreabichsel
manager: tfehr
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 219537aab2015469b6ca6ebed5c00af0190c5187
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111812"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Optimalizace výkonu plánováním dávkových úloh po pracovní době

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

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

   ![Nastavení opakování](media/talent-batch-history-cleanup-recurrence.png)

4. V části **Definovat opakování** nastavte **Počáteční datum** a **Počáteční čas** mimo pracovní dobu nebo víkend. Vyberte **Bez koncového data**. 

   ![Definování počátečního data a času opakování](media/talent-batch-history-cleanup-define-recurrence.png)

5. Vyberte **OK**.

6. V případě potřeby změňte všechny ostatní parametry v podnabídce **Spustit na pozadí** a pak vyberte **OK**.

## <a name="additional-resources"></a>Další prostředky

[Optimalizace výkonu pomocí úloh automatického vyčištění](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]