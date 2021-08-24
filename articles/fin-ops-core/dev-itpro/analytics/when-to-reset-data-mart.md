---
title: Časté otázky týkající se resetování datového tržiště
description: Toto téma poskytuje odpovědi na několik dotazů týkajících se resetování datového tržiště.
author: jinniew
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e5a40342306eb9888b456a865ab2220dccfe65f8ccecc67bf8fc16f907e06977
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767748"
---
# <a name="data-mart-resets-faq"></a>Časté otázky týkající se resetování datového tržiště

Toto téma poskytuje odpovědi na několik dotazů týkajících se resetování datového tržiště. Reset datového tržiště může být časově náročný proces a v závislosti na okolnostech nemusí být požadovaným řešením. Toto téma proto zahrnuje informace o okolnostech, kdy může pomoci reset datového tržiště, a také o okolnostech, kdy je nepravděpodobné, že by to pomohlo.

## <a name="what-is-a-data-mart-reset"></a>Co je resetování datového tržiště?

Reset datového tržiště deaktivuje úlohy integrace, odstraní všechna data datového tržiště a poté znovu povolí integraci.

Aby bylo zajištěno, že nebudou vložena stará data, lze reset datového tržiště spustit až po dokončení stávajících úkolů. Pokud se pokusíte resetovat datové tržiště před dokončením všech úkolů, může se zobrazit zpráva jako: „Obnovení datového tržiště nebylo možné zpracovat z důvodu aktivní úlohy. Prosím zkuste to znovu později.“

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Kdy je třeba provést reset datového tržiště?

Pokud se na vaši situaci vztahuje jeden nebo více z následujících výroků, může vaše organizace těžit z resetování datového tržiště:

- Byla obnovena databáze aplikací.
- Otevřeli jste lístek podpory a technik podpory vám nařídil resetovat datové tržiště jako součást kroku odstraňování problémů.
 
> [!NOTE]
> Proces resetování datového tržiště je ovlivněn počtem transakcí hlavní knihy a rozpočtu ve vaší databázi. V závislosti na počtu transakcí ve vašem systému lze reset datového tržiště dokončit za pouhých 15 minut, nebo to může trvat až čtyři hodiny. Pokud však váš reset trvá déle než čtyři hodiny, doporučujeme vám kontaktovat podporu.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Kdy není resetování datového tržiště vhodné?

Zde jsou některé okolnosti, kdy nedoporučujeme resetovat datové tržiště.

- Máte problémy s výkonem spojené se synchronizací dat.
- Máte opakující se vzor pro resetování z některého z následujících důvodů:

    - **Chybějící data** - Pokud si všimnete, že data chybí, otevřete si u Microsoftu lístek podpory a zkontrolujte formát zprávy a možné problémy se synchronizací dat.
    - **Zaseknutý stav integrace**
    - **Zastaralé záznamy** - Zastaralé záznamy samy o sobě nutně neospravedlňují resetování datového tržiště. Pokud máte velkou datovou sadu, proces resetování bude nějakou dobu trvat, ale je nepravděpodobné, že by vedl ke zlepšení.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Pokud resetuji datové tržiště, přijdu o sestavy, které jsem již vytvořil?

Ne. Vaše sestavy jsou uloženy v tabulkách SQL, které nejsou ovlivněny resetem datového tržiště. Pokud se obáváte ztráty jakýchkoli sestav, které jste navrhli, můžete zálohovat návrhy, které nechcete ztratit. Chcete-li zálohovat návrhy, otevřete návrhář sestav a přejděte na **Společnost \> Společnosti \> Stavební bloky \> Export**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Musí všichni uživatelé opustit systém, než budu moci resetovat datový trh?

Ne. Uživatelé mohou pokračovat v práci v systému během resetování datového tržiště. Uživatelé však nebudou mít přístup k žádným sestavám, které byly vytvořeny pomocí nástroje Financial Reporter, dokud nedojde k dokončení resetu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
