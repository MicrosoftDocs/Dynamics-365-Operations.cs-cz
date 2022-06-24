---
title: Správa uživatelů obchodních partnerů na webech elektronického obchodu B2B
description: Tento článek popisuje, jak přidávat, upravovat a odstraňovat uživatele obchodních partnerů na webech Microsoft Dynamics 365 Commerce elektronického obchodování typu business-to-business (B2B) a v Commerce headquarters.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4a3d1c7bf7e7ea545590315d9e185fa525b5d5e3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860288"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Správa uživatelů obchodních partnerů na webech elektronického obchodu B2B

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak přidávat, upravovat a odstraňovat uživatele obchodních partnerů na webech Microsoft Dynamics 365 Commerce elektronického obchodování typu business-to-business (B2B) a v Commerce headquarters.

> [!NOTE]
> - Článek [Správa B2B obchodních partnerů pomocí zákaznických hierarchií](partners-customer-hierarchies.md) je předpokladem tohoto dokumentu.
> - Ujistěte se, že jste inicializovali entitu typů dokumentů v ústředí Commerce otevřením formuláře **Typy dokumentů** v nabídce **Správa organizace \> Správa dokumentů \> Typy dokumentů**.

Weby elektronického obchodování B2B vyžadují registraci organizací, aby se staly obchodními partnery. Poté, co organizace odešle registrační údaje na web elektronického obchodování B2B, projde požadavek na registraci procesem kvalifikace. Pokud se organizace úspěšně kvalifikuje, je přijata jako obchodní partner.

Poté, co se organizace zaregistruje jako obchodní partner, je uživatel organizace, který inicioval požadavek stát se obchodním partnerem, identifikován jako uživatel - správce - a je mu uděleno oprávnění pro připojení dalších oprávněných uživatelů webových stránek B2B elektronického obchodování. Tito oprávnění uživatelé pak mohou zadávat objednávky jménem obchodního partnera.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Nastavte uživatele - správce - pro nového obchodního partnera

Potenciální obchodní partneři mohou zahájit proces onboardingu na web B2B elektronického obchodování zasláním žádosti o onboarding prostřednictvím odkazu na webu B2B. Poté mohou partneři pomocí přizpůsobitelného formuláře poskytnout podrobnosti, které jsou nutné pro onboarding a registraci. Po odeslání požadavku se zobrazí stránka s potvrzením odeslání. Pokud je podání schváleno, společnost, pro kterou byl požadavek podán, se stává obchodním partnerem a žadatel (uživatel, který inicioval požadavek na onboarding) se stává uživatelem-správcem pro obchodního partnera.

Chcete-li schválit požadavek obchodního partnera v centrále Commerce, postupujte takto.

1. Přejděte na **IT pro maloobchod a velkoobchod \> Plán distribuce**.
1. Spusťte úlohu **P-0001**, chcete-li stáhnout všechny žádosti o zapojení obchodního partnera do centrály Commerce.
1. Po úspěšném spuštění úlohy **P-0001** přejděte na **IT pro maloobchod a velkoobchod \> Zákazník** a spusťte úlohu **Synchronizovat zákazníky a požadavky kanálu**. Po úspěšném spuštění této úlohy se požadavky na přihlášení vytvoří jako potenciální partneři typu **Potenciální zákazník B2B** v centrále Commerce. 
1. Přejděte na **Zákazníci \> Všichni potenciální partneři** a vyberte záznam o novém potenciálním partnerovi a otevřete stránku s jeho podrobnostmi.
1. Na kartě **Obecné** vyberte **Konvertovat \> Schválit/Odmítnout** ke schválení žádosti o onboarding. Když se zobrazí potvrzovací zpráva, potvrďte, že chcete v procesu pokračovat, a poté schvalte požadavek. Schválení změní pole **Stav** záznamu o potenciálním partnerovi na **Schváleno**. Poté je na e-mailovou adresu žadatele odeslán e-mail s potvrzením, že jeho organizace byla schválena jako obchodní partner. Je také vytvořena hierarchie zákazníka, kde je žadatel přidán jako správce pro obchodního partnera.

    > [!NOTE]
    > V současné době je potvrzovací e-mail odeslán ihned po schválení. Budoucí funkce Commerce však umožní správci odesílat e-maily ručně.

1. Přejděte na **IT pro maloobchod a velkoobchod \> Plán distribuce** a spusťte úlohu **1010 (Zákazníci)**, kterou pošlete nově vytvořené záznamy zákazníků a hierarchie zákazníků do databáze kanálů.

> [!NOTE]
> Aby bylo zajištěno, že záznamy o nových zákaznících budou odeslány do databáze kanálů, měl by být alespoň jeden z adresářů přidružených k zákazníkovi zahrnut do adresáře zákazníka přidruženého k online obchodu. Tento proces můžete automatizovat konfigurací adresáře u výchozího zákazníka internetového obchodu tak, aby systém zkopíroval hodnotu adresáře do každého nového zákazníka.

Po synchronizaci záznamů hierarchie zákazníků do databáze kanálů se může žadatel přihlásit na web elektronického obchodování B2B pomocí e-mailové adresy, kterou zadal při odeslání žádosti o onboarding. Uživatelé mohou pomocí postupu registrace definovat heslo pro svůj účet. Informace o tom, jak povolit propojení záznamu poskytovatele identity B2C Azure Active Directory (Azure AD) se záznamem zákazníka B2B, který byl vytvořen při schválení potenciálního zákazníka, najdete v tématu [Povolení automatického propojení](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Informujte B2B potenciální zákazníky, když jsou schváleni nebo zamítnuti

Když schválíte nebo odmítnete žádost o registraci B2B potenciálního zákazníka, může se potenciálnímu zákazníkovi automaticky odeslat e-mailové upozornění.

Chcete-li nastavit e-mailová upozornění v centrále obchodu pro události typu oznámení **Potenciální zákazník B2B schválen** nebo **Potenciální zákazník B2B odmítnut**, postupujte takto.

1. Vytvořte e-mailové šablony pro e-maily, které budou zaslány potenciálním zákazníkům, když se spustí typ oznámení **Potenciální zákazník B2B schválen** nebo **Potenciální zákazník B2B odmítnut**. Informace o zástupných textech, které tyto typy oznámení podporují, naleznete v části [Typy oznámení](../email-templates-transactions.md#notification-types). Informace o způsobu vytvoření e-mailových šablon naleznete v tématu [Vytvoření e-mailové šablony](../email-templates-transactions.md#create-an-email-template).
1. Přidejte typy oznámení **Potenciální zákazník B2B schválen** a **Potenciální zákazník B2B odmítnut** do svého profilu e-mailových oznámení a poté je namapujte na šablony e-mailů, které jste vytvořili. Další nformace o profilech oznámení viz [Nastavení profilu e-mailových oznámení](../email-notification-profiles.md).

## <a name="onboard-additional-business-partner-users"></a>Zapojte další uživatele obchodních partnerů

Uživatel - správce obchodního partnera - může podle potřeby připojit další uživatele obchodních partnerů na web elektronického obchodování B2B.

Chcete-li zapojit další uživatele obchodních partnerů na web B2B elektronického obchodování, postupujte takto.

1. Přihlaste se na web B2B elektronického obchodování jako správce.
1. Přejděte na **Můj účet \> Uživatelé organizace \> Zobrazit podrobnosti** a vyberte **Přidat uživatele**.
1. Zadejte požadované informace a poté vyberte **Uložit**. Stav nového uživatele je nastaven na **Čeká**.

Po spuštění úloh **P-0001** a **Synchronizovat zákazníky a požadavky kanálu** je vytvořen záznam zákazníka typu **Osoba** pro nového uživatele v centrále Commerce. Tento záznam zákazníka je také přidružen k záznamu hierarchie zákazníků příslušného obchodního partnera. Dále je na e-mailovou adresu nového uživatele odeslán e-mail s oznámením, že byl přidán jako uživatel organizace obchodního partnera a nyní se může přihlásit na web elektronického obchodu B2B.

Poté spusťte úlohu **1010 (Zákazníci)** pro synchronizaci nového uživatele obchodního partnera do databáze kanálů.

Po synchronizaci záznamu zákazníka je stav uživatele na webu B2B elektronického obchodování nastaven na **Aktivní** a nový uživatel se může přihlásit na web elektronického obchodu B2B pomocí své e-mailové adresy. Uživatelé mohou pomocí postupu registrace definovat heslo pro svůj účet. Informace o tom, jak povolit propojení záznamu poskytovatele identity B2C Azure AD se záznamem zákazníka B2B, který byl vytvořen v centrále Commerce, najdete v tématu [Povolení automatického propojení](/dynamics365/commerce/identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Upravit údaje o uživateli - obchodním partnerovi

Chcete-li upravit podrobnosti uživatelů - obchodních partnerů, postupujte takto.

1. Přihlaste se na web B2B elektronického obchodování jako správce.
1. Přejděte na **Můj účet \> Uživatelé organizace \> Zobrazit podrobnosti**, vyberte tlačítko **Upravit** (symbol tužky), proveďte požadované změny a poté vyberte **Uložit**. Změny se projeví až po spuštění úloh **P-0001**, **Synchronizovat zákazníky a požadavky kanálu** a **1010 (Zákazníci)**.

## <a name="remove-a-business-partner-user"></a>Odebrat uživatele obchodního partnera

Správce může podle potřeby odebrat stávající uživatele organizace obchodního partnera ze seznamu uživatelů, kteří mají přístup na web elektronického obchodu B2B.
Chcete-li odebrat uživatele obchodního partnera, postupujte takto.
- Přihlaste se na web B2B elektronického obchodování jako správce.
- Přejděte na **Můj účet > Uživatelé organizace \> Zobrazit podrobnosti** a vyberte tlačítko **Odebrat** (symbol "X"). Když se zobrazí potvrzovací zpráva, potvrďte, že chcete uživatele odebrat. Změna se projeví až po spuštění úloh **P-0001**, **Synchronizovat zákazníky a požadavky kanálu** a **1010 (Zákazníci)**.

> [!NOTE]
> Když odeberete uživatele ze seznamu uživatelů, kteří mají přístup na web elektronického obchodu B2B, odpovídající záznam zákazníka se odebere ze záznamu hierarchie zákazníků obchodního partnera. Samotný záznam zákazníka však není vymazán z centrály Commerce.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Zapojení stávajících zákazníků jako obchodních partnerů na webu B2B elektronického obchodu

Správci mohou zapojit obchodní partnery a uživatele přímo do centrály Commerce. Tato funkce je užitečná pro onboarding vašich stávajících obchodních partnerů na webu elektronického obchodu B2B.

Chcete-li zapojit obchodní partnery a uživatele do centrály Commerce, postupujte takto.

1. Vytvořte nebo vyberte zákazníka typu **Organizace**, kterého chcete přidat jako obchodního partnera.
1. Vytvořte nebo vyberte zákazníka typu **Osoba**, kterého chcete přidat jako správce nebo uživatele pro obchodního partnera. Ujistěte se, že primární e-mailové adresy jsou spojeny se zákazníky. Tyto e-mailové adresy slouží k přihlášení na web. 

    > [!NOTE]
    > Systém musí být schopen najít unikátní záznam zákazníka pro uživatele, kteří by měli mít možnost se na web přihlásit. Pokud systém najde více než jednoho zákazníka, který má stejnou primární e-mailovou adresu v právnické osobě, uživatel se nebude moci přihlásit na web.

1. Vytvořte ID hierarchie zákazníků.
1. Do pole **Název** zadejte název.
1. V poli **Organizace** vložte zákazníka organizace obchodního partnera.
1. Na záložce **Hierarchie** vyberte **Přidat**.
1. V poli **Název** vyberte zákazníka typu **Osoba**.
1. Vyberte roli **Správce** pro zákazníka, který má být určen jako správce.
1. Opakováním tohoto procesu přidejte do hierarchie další zákazníky.

## <a name="additional-information"></a>Doplňkové informace

- Všechny úlohy zmíněné v tomto článku lze nakonfigurovat tak, aby se spouštěly podle plánu v dávkovém formátu. Očekává se, že obchodní partneři nakonfigurují dávkové úlohy podle potřeby.
- V současné době lze jako uživatele - správce - označit pouze jeden záznam uživatele / zákazníka a tuto roli lze změnit pouze v centrále Commerce. Neexistuje žádná podpora pro samoobslužné funkce, které obchodním partnerům umožňují určit více správců nebo změnit správce z webů B2B elektronického obchodování.
- Ačkoli pro uživatele mohou být definovány limity výdajů, vynucení limitů výdajů během procesu zadávání objednávek ještě nebylo implementováno.
- Veškerá obchodní logika a ověřování uživatelských prostředí na webových stránkách B2B elektronického obchodování jsou založeny na konfiguraci záznamu zákazníka, který je namapován na uživatele v centrále Commerce.

## <a name="additional-resources"></a>Další prostředky

[Vytvoření webu elektronického obchodu B2B](set-up-b2b-site.md)

[Správa B2B obchodních partnerů pomocí zákaznických hierarchií](partners-customer-hierarchies.md)

[Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B](payment-method.md)

[Nastavte limity množství produktů pro weby B2B elektronického obchodování](quantity-limits.md)

[Přehled číselných řad](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
