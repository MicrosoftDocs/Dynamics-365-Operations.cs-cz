---
title: Globální srážková daň
description: Toto téma poskytuje informace o globální funkci srážkové daně a o tom, jak ji nastavit. Globální funkce srážkové daně je vylepšena u transakcí dodavatelů a zákazníků, takže srážková daň se počítá na úrovni položky.
author: kailiang
ms.date: 01/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 9cb02ba77fa33c839bc2a74811131973d1e5877f
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720216"
---
# <a name="global-withholding-tax"></a>Globální srážková daň

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace o globální funkci srážkové daně a vysvětluje, jak ji nastavit. Tato nová funkce je k dispozici ve verzi 10.0.17 a novější.

Globální funkce srážkové daně je vylepšena u transakcí dodavatelů a zákazníků, takže srážková daň se počítá na úrovni položky. Zůstatek na účtu srážkové daně z nákupních transakcí lze vyrovnat spuštěním úlohy platby srážkové daně proti účtu vyrovnání srážkové daně.

> [!NOTE]
> Globální srážková daň nepodporuje funkci **Spravovat náklady** na stránkách nákupní objednávky, faktury dodavatele a prodejní objednávky.

## <a name="turn-on-global-withholding-tax"></a>Zapnutí globální srážkové daně

1. V pracovním prostoru **Správa funkcí** vyberte **Globální srážková daň** a poté vyberte **Povolit**.
2. Přejděte na **Daň \> Nastavení \> Parametry \> Parametry hlavní knihy** a poté na kartě **Srážková daň** nastavte možnost **Povolit globální srážkovou daň** na **Ano**.
3. Zvolte **Uložit**.
4. Aktualizujte stránku ve webovém prohlížeči.

> [!NOTE]
> Globální funkce srážkové daně nelze zapnout pro země/oblasti, kde již existují lokalizovaná řešení srážkové daně. Mezi tyto oblasti patří mimo jiné Indie, Brazílie, Thajsko, Saúdská Arábie, Irsko, Velká Británie a Spojené státy.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
