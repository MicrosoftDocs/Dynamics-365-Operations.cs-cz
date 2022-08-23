---
title: Konfigurace e-mailového kanálu
description: Tento článek vysvětluje, jak nakonfigurovat e-mailový kanál pro příjem elektronických faktur.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 19339cbcc59e93289609690363b0dd9195a66f6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279863"
---
# <a name="configure-an-email-channel"></a>Konfigurace e-mailového kanálu

[!include [banner](../includes/banner.md)]

Pokud vámi vytvořená funkce elektronické fakturace importuje faktury elektronických dodavatelů z připojených souborů, které jsou přijímány e-mailem, nakonfigurujte kanál e-mailového účtu.

1. Ve službě Regulatory Configuration Service (RCS) vyberte vámi vytvořenou funkci elektronické fakturace. Ujistěte se, že jste vybrali verzi se stavem **Koncept**.
2. Na kartě **Nastavení** vyberte **Přidat**.
3. V rozevíracím dialogovém okně **Vytvořit nastavení funkce** ve skupině polí **Nové** vyberte možnost **Vlastní nastavení**.
4. Ve skupině polí **Typ nastavení** vyberte možnost **Datový kanál**.
5. V poli **Vyberte datový kanál** zadejte **Příchozí e-mail**.
6. Vyberte **Vytvořit**.
7. Vyberte řádek, které jste vytvořili dříve, a poté vyberte možnost **Upravit**.
8. Na kartě **Datový kanál** v části **Parametry** nastavte následující povinná pole.

    | Pole                | Popis |
    |----------------------|-------------|
    | Datový kanál         | Zadejte jedinečný název pro identifikaci datového kanálu. Název může mít maximálně 10 znaků. Název bude odkazován v pravidlech použitelnosti a v připojených aplikacích během komunikačního procesu. |
    | Adresa serveru       | Zadejte adresu serveru poskytovatele e-mailového účtu. Například adresa serveru pro poskytovatele `https://outlook.live.com` je imap-mail.outlook.com. |
    | Port serveru          | Zadejte číslo portu, který používá poskytovatel e-mailového účtu. Například port serveru pro poskytovatele `https://outlook.live.com` je 993. |
    | Tajný kód uživatelského jména     | Zadejte název tajného kódu trezoru klíčů Microsoft Azure, který obsahuje ID uživatelského účtu e-mailu. Tento tajný kód musí být vytvořen v trezoru klíčů a nastaven v prostředí vaší služby. |
    | Tajný kód hesla uživatele | Zadejte název tajného kódu trezoru klíčů, který obsahuje heslo uživatelského účtu e-mailu. |
    | Časový limit              | Maximální časový limit v milisekundách (ms), po který má systém čekat na odpověď. Výchozí hodnota je 10 000 ms (10 sekund). |
    | Hlavní složka          | Zadejte zdroj importu e-mailů nebo složku, ze které má služba zpracovávat e-maily. |
    | Složka archivu       | Zadejte složku, do které se mají ukládat zpracované e-maily. Pokud tuto složku neurčíte, systém ji automaticky vytvoří. |
    | Složka chyb         | Zadejte složku, do které má systém přesunout e-maily, pokud se zpracování nezdaří. Pokud tuto složku neurčíte, systém ji automaticky vytvoří. |
    | Maximální velikost zprávy     | Zadejte maximální velikost jedné zpracovávané zprávy v bajtech. Výchozí hodnota je 20 000 000 bajtů. |
    | Maximální počet zpráv   | Zadejte maximální počet zpracovaných zpráv v rámci jedné akce. Pokud nechcete omezovat počet zpráv, nastavte hodnotu na **0** (nula). |
    | Filtr Od          | Zadejte řetězec, který chcete filtrovat podle adresy odesílatele. Zpracovány budou pouze e-maily, jejichž adresa odesílatele odpovídá filtru. Toto pole je volitelné. Chcete-li zadat více adres odesílatele, použijte jako oddělovače středníky (;). |
    | Filtr předmětu       | Zadejte řetězec, který chcete filtrovat podle předmětu. Zpracovány budou pouze e-maily, jejichž předmět odpovídá filtru. Toto pole je volitelné. Jednoduchá maska jako například **\*něco\* .ext** je podporována; zde každá hvězdička (\*) představuje nula nebo více výskytů jakéhokoli znaku. |
    | Filtr data          | Zadáním kalendářního data definujte maximální stáří zpracovávaných zpráv ve dnech. Toto pole je volitelné. Výchozí hodnota je 30 dní. |
    | Režim zpracování      | <p>Vyberte jednu z následujících možností, chcete-li určit, zda lze všechny přílohy v e-mailu zpracovat společně, nebo zda má být každá příloha zpracována samostatně:</p><ul><li><b>Podle přílohy</b> – Pro každou přílohu v e-mailové zprávě bude vytvořen nový elektronický dokument. Pokud například jeden e-mail obsahuje několik souborů, které obsahují data elektronické faktury, bude každý soubor v systému považován za novou elektronickou fakturu.</li><li><b>Podle e-mailu</b> – Jedna příloha bude považována za základní přílohu a v systému bude vytvořena jedna elektronická faktura. Další přílohy lze použít jako podpůrné soubory.</li></ul> |

9. V sekci **Filtr příloh** přidejte informace o filtrování souborů. Zpracovány budou pouze přílohy, které splňují definovaný filtr. Například **\*.xml** bude filtrovat přílohy, které mají příponu názvu souboru .xml. Název přílohy se používá v Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management během instalace.

    - Pokud v předchozím kroku nastavíte pole **Způsob zpracování** na hodnotu **Podle e-mailu**, zde můžete přidat více filtrů. Název bude identifikovat konkrétní dokument.
    - Pokud nastavíte pole **Způsob zpracování** na hodnotu **Podle přílohy**, můžete přidat pouze jeden filtr.

10. Na kartě **Pravidla použitelnosti** zkontrolujte a aktualizujte kritéria podle potřeby. Hodnota pole **Kanál** se musí rovnat hodnotě, kterou jste zadali do pole **Datový kanál** v kroku 8.
11. Zvolte **Uložit** a zavřete stránku.
