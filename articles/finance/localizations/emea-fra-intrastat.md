---
title: Francouzský Intrastat
description: Tento článek obsahuje informace o deklaraci Intrastat ve Francii.
author: anasyash
ms.date: 07/9/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: e86d7c8f28b1b3df0066a588d380965c21dc98a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887846"
---
# <a name="french-intrastat"></a>Francouzský Intrastat

[!include[banner](../includes/banner.md)]

Společnosti ve Francii, které jsou registrované pro daň z přidané hodnoty (DPH) a které obchodují s ostatními zeměmi Evropské unie (EU), musí deklarovat směnu zboží a služeb do a z Francie. Deklarace d'exchanges de biens (Deklarace obchodu se zbožím nebo DEB) je kombinací seznamu prodejů EU a sestavy Intrastat. Tuto zprávu musíte odeslat měsíčně u veškerého prodeje zboží v rámci Společenství.

Sestavu DEB můžete generovat v jednom ze dvou formátů elektronických textových souborů: SAISUNIC 330 nebo INTRACOM.

V následující tabulce jsou uvedena pole, která jsou obsažena ve francouzské deklaraci Intrastat ve formátu SAISUNIC 330. Tabulka také uvádí úroveň sestavy pole. Pole může mít hodnotu **4** (zjednodušený), **1** (úplný) nebo obojí.

| **Pole**                   | **Úroveň sestavy** |
|-----------------------------|------------------|
| Referenční období         | 4, 1              | 
| Číslo prohlášení       | 4, 1              |
| Číslo řádku                 | 4, 1              |
| Kód ISO země (FR)       | 4, 1              | 
| Doplňkový kód          | 4, 1              | 
| Číslo Siren                | 4, 1              | 
| Kód DPH odběratele        | 4, 1              | 
| Kód směru              | 4, 1              |
| Typ transakce            | 4, 1              | 
| Úroveň povinnosti            | 4, 1              |
| Kód zboží              | 1                | 
| Národní NGP                | 1                | 
| Okres (oddělení)         | 1                |
| Povaha transakce       | 1                | 
| Země původu      | 1                | 
| Země původu - Import | 1                | 
| Konečný cíl - Export | 1                | 
| Hodnota faktury               | 4, 1              | 
| Statistická hodnota           | 1                |
| Čistá hmotnost                  | 1                | 
| Dodatečné jednotky            | 1                |
| Kód přenosu              | 1                | 

V následující tabulce jsou uvedena pole, která jsou obsažena ve francouzské deklaraci Intrastat ve formátu INTRACOM.
Tabulka také uvádí úroveň sestavy pole. Pole může mít hodnotu **4** (zjednodušený), **1** (úplný) nebo obojí.

| **Pole**                   | **Úroveň sestavy**   | 
|-----------------------------|--------------------|
| Kód                        | 4, 1               | 
| Číslo prohlášení       | 4, 1               |
| Číslo řádku              | 4, 1               | 
| Siren                       | 4, 1               |
| Okres (oddělení)         | 1                  |          
| Kód přenosu              | 1                  |          
| Země původu           | 1                  |            
| Povaha transakce       | 1                  |             
| Hodnota faktury               | 4, 1               |             
| Způsoby dodání           | 1                  |           
| Typ transakce            | 4, 1               |            
| Úroveň povinnosti            | 4, 1               |           
| Kód zboží              | 1                  |            
| Národní NGP                | 1                  |            
| Čistá hmotnost                  | 1                  |            
| Statistická hodnota           | 1                  |            
| Dodatečné jednotky            | 1                  |            
| Země původu - Import | 1                  |            
| Konečný cíl - Export | 1                  |            
| Kód DPH odběratele        | 4, 1               |            
| Doplňkový kód          | 4, 1               |           
| Referenční období         | 4, 1               |         

### <a name="set-up-intrastat"></a>Vytvořit Intrastat

1.  V [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) v knihovně Sdílený majetek si stáhněte nejnovější verze následujících konfigurací elektronického výkaznictví (ER) pro přiznání Intrasat:

    - Modul Intrastat
    - Sestava Intrastat
    - Intrastat INTRACOM (FR)
    - Intrastat SAISUNIC (FR)

    Další informace viz [Stažení konfigurace elektronického vykazování ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  V Dynamics 365 Finance přejděte do nabídky **Daň** > **Nastavit** >  **Zahraniční obchod** > **Parametry zahraničního obchodu** a postupujte takto:

    1. Na kartě **Intrastat** na pevné záložce **Elektronické hlášení** v poli **Mapování formátu souboru** vyberte **Intrastat INTRACOM (FR)** nebo **Intrastat SAISUNIC (FR)**.
    2. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat**.
    3. Na pevné záložce **Hierarchie komoditních kódů** v poli **Hierarchie kategorií** vyberte **Intrastat**.
    4. Na pevné záložce **Všeobecné** v poli **Kód transakce** vyberte kód, který se používá pro převody zboží.
    5. V poli **Dobropis** vyberte kód, který se použije pro vrácení zboží.
    6. V poli **Úroveň povinnosti pro vývoz** zadejte úroveň podrobnosti sestavy exportu. Úroveň, kterou vyberete, ovlivní řádky, které se zobrazí v sestavě. Další informace naleznete v tabulkách v úvodu tohoto článku.

3. Přejděte do části **Správa organizace** > **Organizace** > **Právnické osoby**, vyberte svou společnost a postupujte takto:

    1. Na pevné záložce **Registrační čísla** v poli **NAF kód** zadejte svůj kód NAF. Další informace naleznete v tématu [Kódy NAF FR-00003 a čísla Siret](tasks/fr-00003-naf-codes-siret-numbers.md).
    2. Na pevné záložce **Zahraniční obchod a logistika** v sekci **Intrastat** nastavte pole **Export čísla osvobozeného od DPH** a **Import čísla osvobozeného od DPH**.
    3. Na pevné záložce **Daňová registrace** v poli **Daňové registrační číslo** zadejte daňové identifikační číslo (DIČ) vaší společnosti.

4. Chcete-li zadat kódy NAF a DIČ pro zákazníky, přejděte na **Pohledávky** > **Zákazníci** > **Všichni zákazníci** a postupujte takto:

    1. Vyberte odběratele.
    2. Na pevné záložce **Faktura a dodání** v sekci **DPH** do pole **Číslo osvobozené od daně** zadejte číslo osvobozené od daně zákazníka.
    3. Na pevné záložce **Demografie prodeje** do pole **Francouzský siret** zadejte číslo Siret společnosti.
    4. Do pole **Kód NAF** zadejte kód NAF podniku.
    5. Tyto kroky opakujte pro ostatní zákazníky.

5. Chcete-li zadat kódy NAF a DIČ pro dodavatele, přejděte na **Závazky** > **Dodavatelé** > **Všichni dodavatelé** a postupujte takto:

    1. Vyberte dodavatele.
    2. Na pevné záložce **Faktura a dodání** v sekci **DPH** do pole **Číslo osvobozené od daně** zadejte číslo osvobozené od daně dodavatele.
    3. Na pevné záložce **Demografie nákupu** do pole **Francouzský siret** zadejte číslo Siret společnosti.
    4. Do pole **Kód NAF** zadejte kód NAF podniku.
    5. Tyto kroky opakujte pro ostatní dodavatele.

6. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Komprese Intrastatu** a vyberte pole, která mají být porovnána po shrnutí informací Intrastat. Pro francouzský Intrastat vyberte **Statistický postup**, **Stát původu**, **Země/region původu**, **Podmínky doručení**, **Doprava**, **Oprava**, **Země/region**, **Kraj původu/určení**, **Směr**, **Země/oblast odesílatele**, **Stát odesílatele**, **Stát**, **Kód transakce** a **Zboží**.

7. Přejděte do nabídky **Řízení skladu** > **Založit** > **Sklad** > **Sklady**, vyberte sklad a postupujte podle těchto kroků:

    1. Na pevné záložce **Adresy** vyberte **Přidat** nebo **Upravit**.
    2. V dialogovém okně, v poli **Město** vyberte město skladu. Stát města bude pro vaši zprávu DEB použit jako kraj.

### <a name="ngp-codes"></a>Kódy NGP

Ve zprávě DEB se kodifikace produktů skládá z následujících prvků:

  - Osmimístný kód CN8, který představuje celní a statistickou nomenklaturu EU.
  - Je-li to relevantní, jednociferný národní kód položky Nomenklatura Générale des Produits (NGP).

V roce 2021 se NGP vztahuje pouze na tři typy produktů:

  - Některé produkty krav, ovcí a koz
  - Vojenské vybavení
  - Francouzská vína

 Musíte nastavit kódy NGP a přiřadit je k souvisejícím produktům. Pole **NGP** se poté automaticky nastaví na stranu **Deník Intrastat**.

#### <a name="set-up-an-ngp-code"></a>Nastavení kódu NGP

1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Kódy transakcí**.
2. V podokně Akce vyberte možnost **Nový** a vytvořte kód NGP.
3. V poli **NGP** zadejte jednociferný kód.
4. Do pole **Popis** zadejte popis kódu.

#### <a name="assign-an-ngp-code-to-a-product"></a>Přiřazení kódu NGP k produktu

1. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
2. V mřížce vyberte produkt.
3. Na pevné záložce **Zahraniční obchod** v sekci **Intrastat** v poli **NGP** vyberte příslušný kód NGP.

## <a name="intrastat-journal"></a>Deník Intrastat

Přejděte na **Daň** > **Prohlášení** > **Zahraniční** **obchod** > **Intrastat**, kde můžete spravovat své transakce, které se vztahují na zahraniční obchod se zeměmi EU. Další informace naleznete v [Přehledu Intrastat](emea-intrastat.md).

Sloupec **NGP** je specifický pro Francii. Zobrazuje kód NGP pro produkt. Pokud se NGP na produkt nevztahuje, zobrazí se **0** (nula). Můžete upravit kód NGP. Vyberte transakci a poté na kartě **Všeobecné** v sekci **Kódy** v poli **NGP** vyberte požadovaný kód NGP.

### <a name="intrastat-transfer"></a>Přenos Intrastat

Na stránce **Intrastat** v podokně akcí můžete vybrat **Přenos** k automatickému přenosu informací o obchodu uvnitř Společenství z vašich prodejních objednávek, faktury s volným textem, nákupní objednávky, faktury dodavatele, účtenky produktů dodavatele, faktury projektu a objednávky přenosu. Budou přeneseny pouze dokumenty, které mají jako zemi nebo region určení (pro odeslání) nebo zásilku (pro přijetí) zemi EU.

Protože sestava DEB je kombinací EU Sales List a Intrastat report, obsahuje také *trojúhelníkové* transakce, kdy je přímé dodání provedeno z jedné země EU (strana A) do jiné země EU (strana C) a francouzský právní subjekt (strana B) je uprostřed trojúhelníkového obchodu.

### <a name="generate-a-deb-intrastat-report"></a>Vygenerovat sestavu DEB (Intrastat)

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí vyberte **Výstup** > **Sestava**.
3. V dialogovém okně **Sestava Intrastat** nastavte následující pole.

    | Pole            | popis                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Od data        | Vyberte počáteční datum sestavy.                                                                                               |
    | Do data          | Vyberte koncové datum sestavy.                                                                                                 |
    | Generovat soubor    | Tuto možnost nastavte na **Ano**, chcete-li generovat soubor .txt.                                                                                 |
    | Název souboru        | Zadejte název souboru .txt pro sestavu Intrastat.                                                                          |
    | Generovat sestavu  | Tuto možnost nastavte na **Ano**, chcete-li generovat soubor .xml.                                                                                |
    | Název souboru sestavy | Zadejte požadovaný název.                                                                                                            |
    | Pouze oprava | Chcete-li hlásit pouze opravy, nastavte tuto možnost na hodnotu **Ano**. Nastavte ji na **Ne**, chcete-li vykazovat běžné transakce i opravy.         |
    | Směr        | Vyberte **Příjezdy** pro zprávu o příchozích do společenství. Vyberte **Odeslání** pro zprávu o odeslání v rámci komunity. |

## <a name="example"></a>Příklad

Následující příklad ukazuje, jak nastavit Francouzský Intrastat a vytvořit zprávu DEB. Použije právnickou osobu **DEMF**.

1. V [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) v knihovně Sdílený majetek si stáhněte nejnovější verze následujících konfigurací ER pro formát přiznání Intrasat:

    - Modul Intrastat
    - Sestava Intrastat
    - Intrastat INTRACOM (FR)

2. Ve Finance nastavte kód transakce:

    1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Kódy transakcí**.
    2. V podokně akcí zvolte **Nový**.
    3. Do pole **Kód transakce** zadejte **11**.
    4. Do pole **Název** zadejte **Nákup nebo prodej**.
    5. V podokně akcí vyberte **Uložit**.

3.  Nastavte hierarchii produktů:

    1. Přejděte do nabídky **Řízení informací o produktech** > **Nastavení** > **Kategorie a atributy** > **Hierarchie kategorií**.
    2. V mřížce vyberte **Intrastat**. Potom v podokně akcí na kartě **Hierarchie kategorií** ve skupině **Spravovat** zvolte **Uptavit**.
    3. V podokně akcí vyberte možnost **Nový uzel kategorií**.
    4. Do pole **Název** zadejte **Autres Libournais**.
    5. Do pole **Kód** zadejte **2204 21 42**
    6. V podokně akcí vyberte **Uložit**.

4. Přejděte do nabídky **Daň** > **Nastavit** > **Zahraniční obchod** > **Parametry zahraničního obchodu** a postupujte takto:

    1. Na kartě **Intrastat** na pevné záložce **Všeobecné** v poli **Kód transakce** vyberte **11**.
    2. Na pevné záložce **Elektronické hlášení** v poli **Mapování formátu souboru** vyberte **Intrastat INTRACOM (FR)**.
    3. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat**.
    4. Na pevné záložce **Hierarchie komoditních kódů** v poli **Hierarchie kategorií** vyberte **Intrastat**.

5. Nastavení kódu NGP:

    1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Kódy transakcí**.
    2. V podokně akcí zvolte **Nový**.
    3. Do pole **NGP** zadejte **8**.
    4. Do pole **Název popisu** zadejte **NGP 8**.
    5. V podokně akcí vyberte **Uložit**.

6. Přiřazení kódu NGP k produktu:

    1. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
    2. V mřížce vyberte **0001**.
    3. Na pevné záložce **Zahraniční obchod** v poli **NGP** vyberte **8**.
    4. V poli **Zboží** vyberte **2204 21 42**.
    5. V podokně akcí vyberte **Uložit**.

7. Vytvořte prodejní objednávku, která zahrnuje nový produkt:

    1. Přejděte na **Pohledávky** > **Objednávky** > **Všechny prodejní objednávky**.
    2. V podokně akcí zvolte **Nový**.
    3. V dialogovém okně **Vytvořit** **prodejní** **objednávku**, v sekci **Odběratel** vyberte v poli **Účet** **odběratele** hodnotu **100001**.
    4. V sekci **Adresa** v poli **Doručovací adresa** vyberte znaménko plus (**+**) k vytvoření adresy.
    5. V dialogovém okně **Nová adresa** v poli **Název popisu** zadejte **Německo**.
    6. V poli **Země/region** vyberte **DEU**.
    7. Vyberte **OK**.
    8. Vyberte **OK** v dialogovém okně **Vytvoření prodejní objednávky**.
    9. Na pevné záložce **Řádky** **prodejní objednávky** v poli **Číslo položky** vyberte **0001**.
    10. V podokně akcí vyberte **Uložit**.
    11. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
    12. V dialogovém okně **Účtování faktury** na pevné záložce **Parametry** v sekci **Parametr**, v poli **Množství** vyberte **Všechny**. Poté vyberte **OK** pro zaúčtování faktury.

8.  Vytvořit sestavu DEB:

    1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**:
    2. V Podokně akcí. vyberte **Přenos**.
    3. V dialogovém okně **Intrastat (přenos)** v sekci **Parametry** nastavte možnost **Zákaznická faktura** na **Ano**. Pak vyberte **OK**.
    4. Seřaďte transakce podle pole **Datum**. Horní transakce je výsledná transakce. Pole **NGP** se nastaví automaticky.
    5. V podokně akcí vyberte **Výstup** &gt; **Sestava**.
    6. V dialogovém okně **Sestava Intrastat** na pevné záložce **Parametry** v sekci **Datum** vyberte měsíc prodejní objednávky, kterou jste vytvořili.
    7. V sekci **Možnosti exportu** nastavte možnost **Generovat soubor** na **Ano**.
    8. Do pole **Název souboru** zadejte požadovaný název.
    9. Vyberte **OK** a zkontrolujte sestavu.

