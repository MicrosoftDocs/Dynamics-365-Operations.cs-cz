---
title: Možnosti nastavení automatizace faktur dodavatele (Preview)
description: Tento článek popisuje možnosti dostupné pro nastavení a konfiguraci automatizace faktur dodavatele.
author: sunfzam
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86ad68b3dc08bf2c57ab5f9bc6c65bc37c0901e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874834"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Možnosti nastavení pro automatizaci faktur dodavatele

[!include [banner](../includes/banner.md)]

Tento článek popisuje možnosti dostupné pro nastavení a konfiguraci automatizace faktur dodavatele. Funkce automatizace faktur používají následující typy parametrů nastavení:

- Parametry pro automatické použití záloh v importovaných fakturách.
- Parametry pro odesílání importovaných faktur dodavatelů do systému workflowu a párování zaúčtovaných řádků příjemky produktu s nevyřízenými řádky faktury dodavatele.
- Parametry pro úlohy automatizace zpracování na pozadí. Systém automatizace procesů se používá k odeslání importovaných faktur dodavatele do systému workflow. Používá se také k automatickému přiřazování zaúčtovaných řádků příjmů produktů k čekajícím řádkům faktur dodavatele a k provádění ověření shody faktur u ručních faktur, které byly automaticky přiřazeny k řádkům příjmů produktů. Různé obchodní procesy používají tento systém k definování, jak často vybraný proces poběží. Dostupné frekvence pro procesy na pozadí **Přiřadit příjemky produktů k řádkům faktury** a **Odeslat faktury dodavatele do pracovního postupu** zahrnují **Hodina** a **Denně**.

Chcete-li nastavit nebo zobrazit informace o úloze na pozadí, přejděte na **Správa systému \> Nastavení \> Automatizace procesů** a vyberte kartu **Úloha na pozadí**.

Chcete-li dosáhnout bezdotykové automatizace z procesu importu prostřednictvím zaúčtování faktur dodavatele, musíte nastavit pracovní postup pro fakturu dodavatele. Pracovní postup nastavíte tak, že přejděte na **Závazky > Nastavení > Workflow závazků**. Aby fakturu bylo možné zpracovat od začátku až do konce bez ručního zásahu, musíte do své konfigurace workflowu zahrnout automatizovanou úlohu zaúčtování.

## <a name="parameters-for-automatically-applying-prepayments-in-imported-invoices"></a>Parametry pro automatické použití záloh v importovaných fakturách

- **Automaticky použít zálohu na importované faktury** – Když je tato možnost nastavena na **Ano**, systém automaticky vyhledá existující zálohy pro odpovídající nákupní objednávku při importu faktur dodavatele. Pokud jsou nalezeny nějaké zálohy, které lze použít, přidá se jeden další řádek pro použití záloh ve fakturách dodavatele, které se importují.
- **Blokovat proces následné automatizace v případě selhání žádosti o zálohu** – Když je tato možnost nastavena na **Ano**, faktury budou zablokovány, pokud nebude možné použít zálohu. Stejně jako jiné automatizované procesy, jako je proces párování účtenek a odeslání do procesu pracovního prostoru, proces automatizace faktur nevyzvedne zablokované faktury, dokud nebude ručně aplikována platba předem. 

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Parametry pro odesílání importovaných faktur dodavatelů do systému workflow

Pro odesílání importovaných faktur dodavatelů do systému workflow se používají specifické parametry. Kromě to ho se používají určité parametry k automatickému přiřazování zaúčtovaných řádků účtů produktu k nevyřízeným řádkům faktur dodavatelů. Na kartě **Automatizace faktur dodavatele** na stránce **Parametry závazků** jsou parametry, které musíte nastavit, rozděleny do následujících částí:

- Pracovní postup faktur dodavatele
- Spárovat příjemky produktu automaticky

K dispozici jsou následující parametry:

- **Automaticky odesílat importované faktury do workflow** – Pokud nastavíte tuto možnost na **Ano**, importované faktury se budou automaticky odesílat do systému workflow. Pokud je tato možnost nastavena na **Ne**, faktury musí být předloženy ručně. Nastavením této možnosti na **Ano** povolíte bezdotykový proces importu výsledků prostřednictvím zaúčtování.

    Tuto možnost můžete nastavit na **Ano** pouze v případě, že je pro vaši právnickou osobu nastaven aktivní pracovní postup faktury dodavatele. Pracovní postup nastavíte tak, že přejděte na **Závazky \> Nastavení \> Workflow závazků**.

- **Před automatickým odesláním přiřadit příjemky produktů k řádkům faktur** – Pokud tuto možnost nastavíte na **Ano**, importovanou fakturu nelze automaticky odeslat do systému workflow, dokud se množství přiřazené příjemky produktu nerovná množství na faktuře. Nastavením této možnosti na **Ano** povolíte automatické přiřazování zaúčtovaných příjemek produktů k řádkům faktur, pro které je definována zásada třícestného párování. Tento proces poběží tak dlouho, dokud se množství na přiřazené příjemce produktu nebude rovnat množství na faktuře. V tomto okamžiku se faktura automaticky odešle do systému workflow.

    Možnost **Před automatickým odesláním přiřadit příjemky produktů k řádkům faktur** je k dispozici, pouze pokud je vybrána možnost **Povolit ověření párování faktur**. Pokud je vybrána tato možnost, je automaticky vybrána možnost **Automaticky přiřadit příjemky produktů k řádkům faktur**.

- **Pro automatické odeslání do workflow vyžadovat, aby se vypočtené součty rovnaly importovaným součtům** – Pokud tuto možnost nastavíte na **Ano**, fakturu nelze automaticky odeslat do systému workflow, dokud se vypočítané součty pro fakturu nebudou rovnat importovaným součtům. Pokud je tato možnost nastavena na **Ne**, fakturu lze automaticky odeslat do systému workflow, ale nelze ji zaúčtovat, dokud nebudou vypočtené součty opraveny tak, aby odpovídaly importovaným součtům. Pokud neimportujete částku faktury nebo částku DPH, měla by být tato možnost nastavena na **Ne**.
- **Automaticky přiřadit příjemky produktů k řádkům faktur** – Pokud tuto možnost nastavíte na **Ano**, zpracování na pozadí lze použít k automatickému párování zaúčtovaných příjemek produktů k řádkám faktur, pro které je definována zásada třícestného párování. Tento proces bude probíhat, dokud se množství přiřazené příjemky produktu nebude rovnat množství na faktuře nebo dokud nebude dosaženo hodnoty v poli **Počet pokusů o automatické přiřazení**. Proces lze spustit, dokud nebude faktura odeslána do systému workflow.

    Tato možnost je k dispozici, pouze pokud je vybrána možnost **Povolit ověření párování faktur**.

    Pokud nastavíte možnost **Přiřadit příjemky produktů k řádkům faktur před automatickým párováním** na **Ano**, nelze tuto možnost nastavit na **Ne**. Pokud chcete tuto možnost nastavit na **Ne**, musíte nejprve nastavit možnost **Přiřadit příjemky produktů k řádkům faktur před automatickým párováním** na **Ne**.

- **Počet pokusů o automatické přiřazení** – U tohoto procesu můžete určit maximální počet pokusů, které má systém na spárování příjemky produktu s řádkem faktury, než se tento proces označí jako neúspěšný. Po dosažení zadaného počtu pokusů je faktura z automatizovaného zpracování odebrána.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
