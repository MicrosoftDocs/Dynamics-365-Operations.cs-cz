---
title: Optimalizace výkonu plánováním dávkových úloh po pracovní době
description: V tomto tématu se vysvětluje, jak řešit některé problémy s aplikací Microsoft Dynamics 365 Human Resources plánováním dlouho běžících dávkových úloh po pracovní době.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500498"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Optimalizace výkonu plánováním dávkových úloh po pracovní době

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
