---
title: Časté otázky týkající se resetování datového tržiště
description: Tento článek poskytuje odpovědi na několik dotazů týkajících se resetování datového tržiště.
author: jinniew
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d2b20ec7af9f0c6b7899617c2b8fdbf0992d7397
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892385"
---
# <a name="data-mart-resets-faq"></a>Časté otázky týkající se resetování datového tržiště

Tento článek poskytuje odpovědi na několik dotazů týkajících se resetování datového tržiště. Reset datového tržiště může být časově náročný proces a v závislosti na okolnostech nemusí být požadovaným řešením. Tento článek proto zahrnuje informace o okolnostech, kdy může pomoci reset datového tržiště, a také o okolnostech, kdy je nepravděpodobné, že by to pomohlo.

## <a name="what-is-a-data-mart-reset"></a>Co je resetování datového tržiště?

Reset datového tržiště deaktivuje úlohy integrace, odstraní všechna data datového tržiště a poté znovu povolí integraci.

Aby bylo zajištěno, že nebudou vložena stará data, lze reset datového tržiště spustit až po dokončení stávajících úkolů. Pokud se pokusíte resetovat datové tržiště před dokončením všech úkolů, může se zobrazit zpráva jako: „Obnovení datového tržiště nebylo možné zpracovat z důvodu aktivní úlohy. Prosím zkuste to znovu později.“

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Kdy je třeba provést reset datového tržiště?

Pokud se na vaši situaci vztahuje jeden nebo více z následujících výroků, může vaše organizace těžit z resetování datového tržiště:

- **Byla obnovena databáze aplikací**
- **Otevřeli jste lístek podpory** – Technik podpory vám nařídil resetovat datové tržiště jako součást kroku odstraňování problémů.
- **Velké procento zastaralých záznamů** – Zastaralé záznamy samy o sobě nutně neospravedlňují resetování datového tržiště. Vysoké procento zastaralých dat může snížit celkový výkon generování sestav a integrace a vynutit dodatečné využití databázového prostoru. Doporučujeme dokončit reset datového tržiště, abyste odstranili zastaralá data, když je v datovém tržišti více než 80 % zastaralých dat.
 
> [!NOTE]
> Proces resetování datového tržiště je ovlivněn počtem transakcí hlavní knihy a rozpočtu ve vaší databázi. V závislosti na počtu transakcí ve vašem systému lze reset datového tržiště dokončit za pouhých 15 minut, nebo to může trvat až čtyři hodiny. Pokud však váš reset trvá déle než čtyři hodiny, doporučujeme vám kontaktovat podporu.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Kdy není resetování datového tržiště vhodné?

Zde jsou některé okolnosti, kdy nedoporučujeme resetovat datové tržiště.

- Máte problémy s výkonem integrace dat.
- Integrace aplikace Financial Reporter není povolena. 

    - To znamená, že data hlavní knihy již nejsou synchronizována s vaším datovým tržištěm Financial Reporting. Vaše aplikace Financial Reporter možná nedostává aktuální čísla z vašich finančních sestav. K tomu obvykle dochází, pokud Financial Reporter delší dobu nepoužíváte.
    - Budete vyzváni k povolení integrace resetováním datového tržiště. Pokračovat můžete výběrem možnosti **Ano**. Můžete se také rozhodnout resetovat datové tržiště později. Po aktivaci integrace se vaše data hlavní knihy znovu synchronizují do aplikace Financial Reporter. 
- Máte opakující se vzor pro resetování z některého z následujících důvodů:

    - **Chybějící nebo neočekávaná data v sestavě** - Pokud si všimnete, že data chybí, otevřete si u Microsoftu lístek podpory a zkontrolujte formát zprávy a možné problémy se synchronizací dat.
    - **Zaseknutý stav integrace** – Pokud si všimnete, že se stav integrace za běhu zasekl, může to být způsobeno velkým objemem transakcí v systému. Tento stav se vyřeší sám. Pokud si však všimnete, že se stav integrace zasekl na více než čtyři hodiny, otevřete nový lístek podpory u společnosti Microsoft. 
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Pokud resetuji datové tržiště, přijdu o sestavy, které jsem již vytvořil?

Ne. Vaše sestavy jsou uloženy v tabulkách SQL, které nejsou ovlivněny resetem datového tržiště. Pokud se obáváte ztráty jakýchkoli sestav, které jste navrhli, můžete zálohovat návrhy, které nechcete ztratit. Chcete-li zálohovat návrhy, otevřete návrhář sestav a přejděte na **Společnost \> Společnosti \> Stavební bloky \> Export**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Musí všichni uživatelé opustit systém, než budu moci resetovat datový trh?

Ne. Uživatelé mohou pokračovat v práci v systému během resetování datového tržiště. Uživatelé však nebudou mít přístup k žádným sestavám, které byly vytvořeny pomocí nástroje Financial Reporter, dokud nedojde k dokončení resetu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
