---
title: Importovat uživatele ze služby Azure Active Directory
description: Tento postup mohou použít správci systému k ručnímu importu vybraných uživatelů nebo k importu velkého počtu uživatelů ze služby Azure Active Directory.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce8c98add0c6d5fb07b3ba5338037d9a12b1d8e50a2d2039b0231d3d305c9ebe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748281"
---
# <a name="import-users-from-azure-active-directory"></a>Importovat uživatele ze služby Azure Active Directory

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Import vybraných uživatelů

Tento postup mohou použít správci systému k importu vybraných uživatelů ze služby Azure Active Directory (Azure AD).

1. Uživatel bude importován spolu s aktuální společností relace jako výchozí společností. Před importem uživatelů změňte v případě potřeby aktuální společnost.
2. Přejděte do nabídky **Správa systému > Uživatelé > Uživatelé**.
3. Klikněte na možnost **Importovat uživatele**.
4. Vyberte uživatele, kteří mají být importováni, a vyberte příkaz **Importovat uživatele**.

Po dokončení importu bude nutné přiřadit role uživatelům.

## <a name="import-users-in-bulk"></a>Hromadné importování uživatelů

Tento postup mohou použít správci systému pro import velkého počtu uživatelů ze služby Azure Active Directory.
Upozorňujeme, že při použití možnosti Dávkový import není možné vybrat uživatele.

## <a name="run-the-import-as-a-batch-job"></a>Spuštění importu jako dávkové úlohy
1. Uživatel bude importován spolu s aktuální společností relace jako výchozí společností. Před importem uživatelů změňte v případě potřeby aktuální společnost.
2. Přejděte do nabídky **Správa systému > Uživatelé > Uživatelé**.
3. Klikněte na **Dávkový import**.
4. Rozbalte sekci **Spustit na pozadí**.
4. V poli **Dávkové zpracování** vyberte hodnotu **Ano**.
6. V poli **Skupina dávek** zadejte nebo vyberte hodnotu. Tento krok je volitelný.  
7. Vyberte hodnotu **Ano** v poli **Soukromý**. Tento krok je volitelný.  
8. Vyberte hodnotu **Ano** v poli **Kritická úloha**. Tento krok je volitelný.  
9. Vyberte volbu v poli **Kategorie monitorování**.
10. Klikněte na tlačítko **OK**.

Po dokončení importu bude nutné přiřadit role uživatelům.

## <a name="run-in-a-sandbox-environment"></a>Spuštění v prostředí sandbox
1. Vyberte možnost **Dávkový import**.
2. Vyberte **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]