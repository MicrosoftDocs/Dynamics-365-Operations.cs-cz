---
title: Spravujte uživatele - obchodní partnery - na webech B2B elektronického obchodování
description: Toto téma popisuje, jak mohou správci přidávat, upravovat a mazat uživatele - obchodní partnery - na webech elektronického obchodování typu business-to-business (B2B).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7c1bd8d9cb494cef78fa7c14f6c391821d48749a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799846"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Spravujte uživatele - obchodní partnery - na webech B2B elektronického obchodování

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak mohou správci přidávat, upravovat a mazat uživatele - obchodní partnery - na webech elektronického obchodování typu business-to-business (B2B).

Weby elektronického obchodování B2B vyžadují registraci organizací, aby se staly obchodními partnery. Poté, co organizace odešle registrační údaje na web elektronického obchodování B2B, projde procesem kvalifikace. Pokud se organizace úspěšně kvalifikuje, je přijata jako obchodní partner.

Poté, co se organizace zaregistruje jako obchodní partner, je uživatel organizace, který inicioval požadavek stát se obchodním partnerem, identifikován jako uživatel - správce - a je mu uděleno oprávnění pro připojení dalších oprávněných uživatelů webových stránek B2B elektronického obchodování. Tito oprávnění uživatelé pak mohou zadávat objednávky jménem obchodního partnera.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>Zapněte funkci B2B elektronického obchodování v centrále Commerce

Funkce B2B elektronického obchodování v centrále Commerce umožňuje organizacím přijímat obchodní partnery a definovat uživatele - správce. Tato funkce také umožňuje správcům vytvářet a spravovat uživatele a týmy obchodních partnerů a přiřazovat jim konkrétní role. Nakonec umožňuje uživatelům - obchodním partnerům - vytvářet šablony objednávek a využívat stávající objednávky k přeuspořádání produktů.

Chcete-li zapnout funkci B2B elektronického obchodování v centrále Commerce, postupujte následovně.

1. Přejděte na **Pracovní prostory \> Správa funkcí**.
1. Na kartě **Všechny** filtrujte pole **Modul** použitím výrazu **Maloobchodní a velkoobchodní prodej**.
1. Najděte a vyberte funkci s názvem **Povolit využití funkcí B2B eCommerce** a potom vyberte **Povolit nyní**.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Vytvořte číselnou sekvenci a přidejte ji do sdílených parametrů Commerce

Číselné řady v aplikaci slouží ke generování čitelných, jedinečných identifikátorů pro hlavní datové záznamy a záznamy transakcí, které požadují identifikátory. Další informace o číselných řadách naleznete v tématu [Přehled číselných řad](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Chcete-li vytvořit číselnou sekvenci a přidat ji do sdílených parametrů Commerce v centrále Commerce, postupujte takto.

1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Číselné řady \> Číselné řady** a vytvořte číselnou sekvenci.
1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Parametry \> Sdílené parametry Commerce** a přidejte novou číselnou sekvenci do odkazu **ID hierarchie zákazníků**.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Nastavte uživatele - správce - pro nového obchodního partnera

Potenciální obchodní partneři mohou zahájit proces přihlášení na web B2B elektronického obchodování zasláním žádosti o přihlášení prostřednictvím odkazu na webu. Poté, co potenciální uživatel - obchodní partner - vybere odkaz, může poskytnout podrobnosti, které jsou vyžadovány pro zprovoznění a registraci. Po odeslání požadavku se zobrazí stránka s potvrzením odeslání. Pokud je podání schváleno, stane se žadatel (tj. uživatel, který inicioval registrační požadavek) uživatelem - správcem - obchodního partnera.

Chcete-li schválit a nastavit uživatele - správce obchodního partnera - v centrále Commerce, postupujte takto.

1. Přejděte na **IT pro maloobchod a velkoobchod \> Plán distribuce**.
1. Spusťte úlohu **P-0001**, chcete-li stáhnout všechny žádosti o zapojení obchodního partnera do centrály Commerce.
1. Po úspěšném spuštění úlohy **P-0001** přejděte na **IT pro maloobchod a velkoobchod \> Zákazník** a spusťte úlohu **Synchronizujte zákazníky a obchodní partnery z asynchronního režimu** práce. Po úspěšném spuštění této úlohy se požadavky na přihlášení vytvoří jako záznamy o potenciálních partnerech v centrále Commerce. Pole **ID typu** těchto záznamů je nastaveno na **Potenciální partner B2B**.
1. Přejděte na **Zákazníci \> Všichni potenciální partneři** a otevřete stránku potenciálního partnera.
1. Vyberte záznam o potenciálním partnerovi pro nového obchodního partnera a otevřete stránku s podrobnostmi o potenciálním partnerovi.
1. Na kartě **Všeobecné** vyberte **Konvertovat \> Schválit/Odmítnout** ke schválení nebo zamítnutí žádosti o zprovoznění. Když se zobrazí potvrzovací zpráva, potvrďte, že chcete v procesu pokračovat, a schvalte požadavek. Poté je na e-mailovou adresu žadatele odeslán e-mail s potvrzením, že jeho organizace byla schválena jako obchodní partner.

    Jakmile žádost schválíte, pole **Stav** záznamu o potenciálním partnerovi se nastaví na **Schváleno**. V systému jsou navíc vytvořeny dva nové záznamy o zákaznících: záznam zákazníka **Typ organizace** pro organizaci obchodního partnera a **Typ osoba** pro žadatele. Vytvoří se také záznam hierarchie zákazníků pro obchodního partnera. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. Přejděte na **IT pro maloobchod a velkoobchod \> Plán distribuce** a spusťte úlohu **1010** (**Zákazníci**), chcete-li poslat nově vytvořené záznamy zákazníků a hierarchie zákazníků do databáze kanálů.

Po schválení požadavku a po synchronizaci záznamů zákazníka a hierarchie zákazníků do databáze kanálů se může žadatel přihlásit na web elektronického obchodování B2B pomocí e-mailové adresy, kterou zadal při odeslání žádosti. Uživatelé mohou pomocí postupu registrace definovat heslo pro svůj účet.

## <a name="onboard-additional-business-partner-users"></a>Zapojte další uživatele obchodních partnerů

Uživatel - správce obchodního partnera - může podle potřeby připojit další uživatele obchodních partnerů na web elektronického obchodování B2B.

Chcete-li zapojit další uživatele obchodních partnerů na web B2B elektronického obchodování, postupujte takto.

1. Přihlaste se na web B2B elektronického obchodování jako správce.
1. Přejděte na **Můj účet \> Uživatelé organizace \> Zobrazit podrobnosti** a vyberte **Přidat uživatele**.
1. Zadejte požadované informace a poté vyberte **Uložit**. Stav nového uživatele je nastaven na **Čeká**.

    Po spuštění úloh **P-0001** a **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** je vytvořen záznam zákazníka **Typ osoba** nového uživatele v centrále Commerce. Tento záznam zákazníka je také přidružen k záznamu hierarchie zákazníků příslušného obchodního partnera. Dále je na e-mailovou adresu nového uživatele odeslán e-mail s oznámením, že byl přidán jako uživatel organizace obchodního partnera a nyní se může přihlásit na web elektronického obchodu B2B.

1. Spusťte úlohu **1010** (**Zákazníci**) pro synchronizaci nového uživatele obchodního partnera s databází kanálů.

Po synchronizaci záznamu zákazníka je stav uživatele na webu B2B elektronického obchodování nastaven na **Aktivní** a nový uživatel se může přihlásit na web elektronického obchodu B2B pomocí své e-mailové adresy. Uživatelé mohou pomocí postupu registrace definovat heslo pro svůj účet.

## <a name="edit-business-partner-user-details"></a>Upravit údaje o uživateli - obchodním partnerovi

Chcete-li upravit podrobnosti uživatelů - obchodních partnerů, postupujte takto.

1. Přihlaste se na web B2B elektronického obchodování jako správce.
1. Přejděte na **Můj účet \> Uživatelé organizace \> Zobrazit podrobnosti**, vyberte tlačítko **Upravit** (symbol tužky), proveďte požadované změny a poté vyberte **Uložit**. Změny se projeví až po spuštění úloh **P-0001**, **Synchronizace zákazníků a obchodních partnerů z asynchronního režimu** a **1010** (**Zákazníci**).

## <a name="remove-a-business-partner-user"></a>Odebrat uživatele obchodního partnera

Správce může podle potřeby odebrat stávající uživatele organizace obchodního partnera ze seznamu uživatelů, kteří mají přístup na web elektronického obchodu B2B.

Chcete-li odebrat uživatele obchodního partnera, postupujte takto.

1. Přihlaste se na web B2B elektronického obchodování jako správce.
1. Přejděte na **Můj účet \> Uživatelé organizace \> Zobrazit podrobnosti** a vyberte tlačítko **Odebrat** (symbol "X"). Když se zobrazí potvrzovací zpráva, potvrďte, že chcete uživatele odebrat. Změna se projeví až po spuštění úloh **P-0001**, **Synchronizace zákazníků a obchodních partnerů z asynchronního režimu** a **1010** (**Zákazníci**).

> [!NOTE]
> Když odeberete uživatele ze seznamu uživatelů, kteří mají přístup na web elektronického obchodu B2B, odpovídající záznam zákazníka se odebere ze záznamu hierarchie zákazníků obchodního partnera. Samotný záznam zákazníka však není vymazán z centrály Commerce.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Nábor obchodního partnera a uživatelů v centrále Commerce

Správci mohou zapojit obchodní partnery a uživatele přímo do centrály Commerce.

Chcete-li zapojit obchodní partnery a uživatele do centrály Commerce, postupujte takto.

1. Vytvořte záznam zákazníka **Typ organizace** pro organizaci obchodního partnera.
1. Vytvořte záznamy zákazníků **Typ Osoba** pro uživatele obchodního partnera. Ujistěte se, že je pro každého zákazníka zadána primární e-mailová adresa.
1. Pro každý záznam zákazníka **Typ osoba**, který musí být označen jako uživatel - správce organizace obchodního partnera - na pevné záložce **Maloobchod** nastavte možnost **Správce B2B** na **Ano**.
1. Vytvořte ID hierarchie zákazníků. Do pole **Název** zadejte název.
1. V poli **Organizace** vložte zákazníka organizace obchodního partnera.
1. Vyberte **Přidat** a pak vyberte zákazníka v poli **Jméno**.
1. Opakováním tohoto procesu přidejte do hierarchie další zákazníky.

## <a name="additional-information"></a>Doplňkové informace

- Všechny úlohy zmíněné v tomto tématu lze nakonfigurovat tak, aby se spouštěly podle plánu v dávkovém formátu. Očekává se, že obchodní partneři nakonfigurují dávkové úlohy podle potřeby.
- V současné době lze jako uživatele - správce - označit pouze jeden záznam uživatele / zákazníka a tuto roli lze změnit pouze v centrále Commerce. Neexistuje žádná podpora pro samoobslužné funkce, které obchodním partnerům umožňují určit více správců nebo změnit správce z webů B2B elektronického obchodování.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Ačkoli pro uživatele mohou být definovány limity výdajů, vynucení limitů výdajů během procesu zadávání objednávek ještě nebylo implementováno.
- Veškerá obchodní logika a ověřování uživatelských prostředí na webových stránkách B2B elektronického obchodování jsou založeny na konfiguraci záznamu zákazníka, který je namapován na uživatele v centrále Commerce.

## <a name="additional-resources"></a>Další prostředky

[Nastavení webu elektronického obchodování B2B](set-up-b2b-site.md)

[Vytvářejte hierarchie modelování org pro organizace B2B](org-model.md)

[Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B](payment-method.md)

[Nastavte limity množství produktů pro weby B2B elektronického obchodování](quantity-limits.md)

[Přehled číselných řad](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]