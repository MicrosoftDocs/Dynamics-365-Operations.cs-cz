---
title: Nastavení účetních skupin pro DPH
description: DPH je vypočítáno a zaúčtováno do hlavních účtů, které jsou zadány v části Účetní skupiny.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30870ea17ea73e48467698166ba14a9184f5a3b1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144805"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Nastavení účetních skupin pro DPH

[!include [banner](../../includes/banner.md)]

DPH je vypočítáno a zaúčtováno do hlavních účtů, které jsou zadány v části Účetní skupiny. Účetní skupiny jsou připojeny k jednotlivým kódům DPH. Pro každý kód DPH můžete nastavit individuální účetní skupiny hlavní knihy pro DPH; můžete použít jednu účetní skupinu hlavní knihy pro všechny kódy DPH nebo můžete ke všem kódům DPH přiřadit několik účetních skupin hlavní knihy. Tento záznam používá ukázkovou společnost DEMF. 

1. Přejděte na **Navigační podokno > Moduly > Daň > Nastavení > DPH > Účetní skupiny**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Skupina zaúčtování hl. knihy**.
4. Zadejte hodnotu do pole **Popis**.
5. V poli **DPH na výstupu** vyberte hlavní účet pro odchozí DPH, které jsou splatné finančnímu úřadu. DPH se vybírají jménem finančního úřadu při prodeji zdanitelného zboží a služeb.  
6. V poli **Pohledávka DPH** vyberte hlavní účet pro příchozí DPH, které jsou přijatelné od finančního úřadu. Dodavatelé vybírají daně jménem finančního úřadu při nákupu zdanitelného zboží a služeb. Toto pole není k dispozici v případě, že je vybrána možnost Použít daňové předpisy pro DPH na stránce **Parametry hlavní knihy**. DPH zaplacená dodavatelům je místo toho připsána na stejný účet, jako při nákupu.   
7. V poli **Importní DPH – výdaj** vyberte hlavní účet pro zaúčtování odečitatelných importních daní, které nejsou dodavateli nárokovány ani vykazovány finančnímu úřadu jako součást stornovacího poplatku GST/HST pro EU. Možnosti **Použít daň** musíte vybrat pro **kód DPH** ve **skupině DPH**, která je použitá v transakci. Toto pole nebude k dispozici v případě, že je vybrána možnost **Použít daňové předpisy pro DPH** na stránce **Parametry hlavní knihy**.   
8. V poli **Splatná importní DPH** vyberte hlavní účet pro zaúčtování příchozích importních daní, které jsou splatné finančním úřadům. Možnosti **Použít daň** musíte vybrat pro **kód DPH** ve **skupině DPH** pro zaúčtování hodnoty v části **Použít daň**. Pokud je vybrána možnost **Použít daňové předpisy pro DPH** na stránce **Parametry hlavní knihy**, protiúčet je zaúčtován na výdajový účet transakce.   
9. V poli **Účet vyrovnání** vyberte hlavní účet na který bude zaúčtován čistý zůstatek účtů hlavní knihy podle pole **Splatná importní DPH** a **DPH na vstupu**. Zůstatek se vytvoří při provedení vyrovnání prodejní daně a zaúčtování.  Pokud je finančnímu úřadu pro období vyrovnání přidružen k účtu dodavatele, zůstatek se zaúčtuje namísto toho na účet dodavatele.
10. V poli **Platební sleva dodavatele** vyberte hlavní účet pro zaúčtování platební slevy pro kódy DPH, které jsou přidružené k této skupině zaúčtování hlavní knihy. Toto pole je nepovinné a pokud není zadán žádný účet, použije se hlavní účet ze seznamu **Kódy platebních slev**. Může být užitečné použití různých účtů pro každou **Skupinu zaúčtování hlavní knihy**, pokud používáte možnost Stornovat DPH u platební slevy pro skupiny DPH.  
11. V poli **Platební sleva odběratele** vyberte hlavní účet pro zaúčtování platební slevy pro **Kódy DPH**, které jsou přidružené k této **Skupině zaúčtování hlavní knihy**. Toto pole je nepovinné a pokud není zadán žádný účet, použije se hlavní účet ze seznamu **Kódy platebních slev**. Může být užitečné použití různých účtů pro každou **Skupinu zaúčtování hlavní knihy**, pokud používáte možnost Stornovat DPH u platební slevy pro **skupiny DPH**.  
12. Klikněte na možnost **Uložit**.

