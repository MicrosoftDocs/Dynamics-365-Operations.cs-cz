---
title: Správa odpočtů pomocí pracovní plochy odpočtu
description: Toto téma popisuje, jak můžete používat pracovní plochu odpočtu ke zpracování plateb odběratelů, které zahrnují odpočty.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: bf98529176fbed368708ea925f542a70f2936037
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500395"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Správa odpočtů pomocí pracovní plochy odpočtu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak můžete používat pracovní plochu odpočtu ke zpracování plateb odběratelů, které zahrnují odpočty.

Zákazník, který má dostat rabat, se může rozhodnout nečekat na jeho vyplacení. Místo toho může zákazník odeslat platbu, která zahrnuje odpočet částky rabatu. Abyste zpracovali tento typ transakce, můžete použít pracovní plochu odpočtu ke spárování odpočtů s otevřenými kreditními transakcemi, rozdělení srážek, zamítnutí srážek a odpisu odpočtů.

> [!NOTE]
> Pracovní plocha odpočtu je již dlouhou dobu součástí prodejních a marketingových funkcí v aplikaci Microsoft Dynamics 365 Supply Chain Management. Nyní však byla vylepšena tak, aby fungovala i s novějším modulem **Správa odpočtů**. Toto téma popisuje, jak v pracovní ploše odpočtu používat starší funkce i funkce Správy odpočtů. Pokud však nemáte [ve vašem systému zapnut modul **Správa slev**](rebate-management-enable.md), některé ze zde popsaných funkcí nebudou k dispozici.

## <a name="prerequisites"></a>Předpoklady

### <a name="set-up-the-old-deduction-management-system"></a>Nastavení starého systému správy odpočtů

Pracovní plochu odpočtu můžete použít společně se starými funkcemi správy odpočtů v Supply Chain Management, i když nepoužíváte modul **Správa slev**. Nejprve však musíte připravit svůj systém podle popisu v této části.

Než budete moci použít pracovní plochu odpočtu, musíte dokončit úlohy nastavení, které jsou popsány v článku [Nastavení správy odpočtů](/dynamicsax-2012/appuser-itpro/set-up-deduction-management). Dále byste měli mít nastavený určitý typ smlouvy o rabatu pro odběratele: buď rabat odběratele, jak je popsán v článku [Nastavení a údržba odběratelských rabatů](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates), nebo rabat obchodní náhrady.

Pokud uplatňujete odpočet na zákazníkův rabat, musíte splnit tyto úkoly:

- [Nastavte rabaty zákazníků](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- Schvalte a zpracujte rabat, abyste mohli použít pracovní plochu odpočtu.

Pokud uplatňujete odpočet na rabat obchodní náhrady, musíte splnit tyto úkoly:

- Nastavit zpětnou fakturaci.
- Použít zpětnou fakturaci.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Konfigurace pohledávek a odpočtů

Systém zaznamenává všechny události odpočtu do deníku nároků. Váš systém proto musí obsahovat deník, který lze k tomuto účelu použít. Pokud ještě nemáte deník nároků, založte si jej. Tento deník je nutný k vytváření odpočtů přímo v pracovní ploše odpočtu, ve vypořádání zákazníků nebo stránce zákazníka.

Chcete-li nastavit nový deník nároků pro odpočty, postupujte takto.

1. Přejděte na položky **Hlavní kniha \> Nastavení deníku \> Názvy deníku**.
1. Vyberte položku **Nový** a nastavte následující pole pro nový deník:

    - **Název** – Zadejte jedinečný název deníku nároků.
    - **Popis** - Zadejte popis nového deníku.
    - **Typ deníku** – Vyberte *Denní*.
    - **Číselná řada dokladů** – Přiřaďte stávající číselnou řadu. Případně vytvořte novou číselnou řadu s typem oboru Společnost a přiřaďte ji k novému deníku.

1. Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.
1. Na kartě **Srážky** nastavte na záložce **Všeobecné** pole **Název deníku nároků** na název deníku, který jste právě vytvořili.
1. Na záložce **Vratka** zadejte následující pole:

    - **Vytvořit vratku** – Nastavením této možnosti určíte, co má systém dělat, když je schválen požadavek na základě množství:

        - *Ano* – Vytvořit vratku.
        - *Ne* - Vytvořit zápornou prodejní objednávku.

    - **Vytvoření bez přiložené faktury** – Výběrem hodnoty určete, co má systém dělat, když je schválen nárok na základě množství, ale není připojena žádná faktura:

        - *Přijmout* – Vytvořit vratku.
        - *Varování* – Vytvořit vratku, ale zobrazit následující varovnou zprávu: „Nárok není připojen k faktuře.“
        - *Chyba* – Nevytvářet vratku a zobrazit následující varovnou zprávu: „Nárok není připojen k faktuře.“ Aktualizace byla zrušena."

    - **Před schválením odpočtu vytvořit vratku** – Tuto možnost nastavte na *Ano*, pokud lze vratky vytvořit před schválením nároku. Toto nastavení platí pouze pro nároky založené na množství, kde je možnost **Vytvořit vratku** nastavena na *Ano*.

### <a name="configure-general-ledger-parameters"></a>Konfigurace parametrů hlavní knihy

Když systém vytvoří deník nároků pro nový odpočet, vytvoří také dvě nové zákaznické transakce: jednu pro protiúčet částky nároku oproti původní faktuře a jednu pro registraci dluhu zákazníka k částce nároku (protože nárok dosud nebyl schválen). Proto musíte svůj systém nastavit tak, aby jeden doklad mohl mít více zákaznických řádků.

Chcete-li povolit více zákaznických řádků v jednom dokladu, postupujte takto.

1. Přejděte na **Hlavní kniha \> Nastavení hlavní knihy \> Parametry hlavní knihy**.
1. Na kartě **Hlavní kniha** nastavte na záložce **Všeobecné** možnost **Povolit více transakcí v rámci jednoho dokladu** na *Ano*.
1. Pokud se zobrazí varovná zpráva, přijměte změnu stiskem tlačítka **Zavřít**.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Vytvořte důvody pro odpočet

Systém vyžaduje, aby uživatelé zadali důvod každého odpočtu, který zadají přímo v pracovní ploše odpočtu, vypořádání zákazníka nebo stránce zákazníka. Důvod určuje, jak se s odpočtem zachází, když je schválen.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Důvody srážky**.
1. Výběrem položky **Nový** přidejte řádek do mřížky a poté pro něj nastavte následující pole:

    - **Důvod nároku** – Zadejte jedinečný název důvodu.
    - **Popis** - Zadejte popis důvodu a poskytněte další informace o tom, jak by měl být použit.
    - **Základ nároku** - Vyberte základ pro důvod nároku:

        - *Na základě ceny* – Po schválení se vytvoří dobropis s volným textem.
        - *Na základě množství* – Po schválení se vytvoří záporná prodejní objednávka nebo vratka.

    - **Kód důvodu vratky** – Vyberte kód důvodu vratky, který chcete použít jako **Kód důvodu vrácení** pro vratku.
    - **Typ** – Vyberte typ odpočtu. Hodnota **Protiúčet odpočtu** pro vybraný typ bude použita k nastavení pole **Protiúčet odpočtu** při vytvoření odpočtu nebo nároku. Typy odpočtu jsou definovány na stránce **Typy odpočtu** (**Prodej a marketing \> Obchodní náhrady \> Srážky \> Typy odpočtu**).
    - **Účet pro zaúčtování nároku** – Toto pole je k dispozici pouze v případě, když je pole **Základ nároku** nastaveno na hodnotu *Na základě ceny*. Když je schválen nárok na základě ceny, systém přiřadí účet hlavní knihy, který zde vyberete jako **Hlavní účet** pro koncept dobropisu s volným textem.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>Nastavení pravidelného úkolu vypořádání schválených odpočtů

U odpočtů, které jsou vytvořeny pomocí příkazu **Nový odpočet** v pracovní ploše odpočtu, vypořádání zákazníka nebo stránce zákazníka, můžete nastavit pravidelný úkol *Vypořádat schválené odpočty*, který automaticky porovná odpočty a položky dal, které mají shodné hodnoty **ID odpočtu** a částky.

Chcete-li naplánovat tento úkol, přejděte do nabídky **Prodej a marketing \> Periodické úkoly \> Vypořádat schválené odpočty** a nastavte možnosti, filtry a plán, stejně jako u jiných typů pravidelných úkolů.

> [!NOTE]
> Pokud je možnost **Automatické vypořádání** nastavena na kartě **Vyrovnání** stránky **Parametry pohledávek** (**Pohledávky \> Nastavení \> Parametry pohledávek**) na *Ano*, periodický úkol *Vypořádat schválené odpočty* nic neudělá, protože kredit bude automaticky vyrovnán.

## <a name="create-a-deduction"></a>Vytvoření odpočtu

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Vytvořte záznam deníku odpočtů pomocí deníku plateb zákazníků

Chcete-li vytvořit záznam deníku odpočtu, postupujte takto.

1. Přejděte na **Pohledávky \> Platby \> Deník plateb zákazníkovi**.
1. Chcete-li přidat řádek do mřížky, klikněte na tlačítko **Nový**.
1. V poli **Název** pro nový řádek vyberte název deníku.
1. V podokně akcí zvolte **Řádky**.
1. Zadejte datum, účet společnosti a číslo účtu zákazníka.
1. V poli **Faktura** vyberte fakturu, ke které je odpočet přidružen.
1. V poli **Dal** zadejte částku, kterou zákazník zaplatil.
1. Výběrem tlačítka **OK** potvrďte, že je částka nižší než celková částka označené transakce.
1. Zvolte typ protiúčtu a protiúčet.
1. Na panelu nástrojů nad mřížkou vyberte **Srážky**.
1. Na stránce **Srážky** v podokně Akce přidejte výběrem položky **Nový** řádek do mřížky. Pole **ID odpočtu** pro nový řádek se nastaví automaticky.
1. V poli **Typ** vyberte typ odpočtu.
1. V poli **Částka** zadejte částku, která se zobrazuje v poli **Zůstatek** pod seznamem odpočtů. Tato částka představuje částku, kterou zákazník odečetl z platby.
1. Zavřete stránku **Odpočet**. Vrátíte se na stránku **Platby zákazníků**, kde se nyní zobrazuje nový řádek pro odpočet.
1. V podokně akcí vyberte možnost **Ověřit \> Ověřit**. Obdržíte následující zprávu: „Deník je v pořádku.“
1. V podokně akcí zvolte **Zaúčtovat**.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Vytvoření odpočtu pomocí pracovní plochy odpočtu

Chcete-li vytvořit nový odpočet na pracovní ploše odpočtu, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. V podokně akcí zvolte **Udržovat \> Nový odpočet**.

    V dialogovém okně **Nový odpočet** je pole **ID odpočtu** nastaveno na základě číselné řady **ID odpočtu**, která je definována na stránce **Parametry správy obchodních náhrad** (**Prodej a marketing \> Nastavení \> Obchodní náhrady \> Parametry správy obchodních náhrad**).

1. Nastavte následující pole:

    - **Zákaznický účet** – Vyberte zákaznický účet, na který se odpočet vztahuje.
    - **Externí číslo nároku** – Zadejte referenci nároku od zákazníka.
    - **Částka nároku** – Zadejte částku nároku zahrnující daň. Hodnota musí být kladná.
    - **Měna** – Vyberte měnu pro odpočet. Výchozí hodnota je měna, která je nastavena pro vybraný zákaznický účet.
    - **Základ nároku** – Vyberte základ nároku. Základ nároku určuje typ kreditní transakce, která je vytvořena po schválení odpočtu nebo nároku.

        - *Na základě ceny* – Bude vytvořen návrh faktury s volným textem.
        - *Na základě množství* – Vytvoří se záporná prodejní objednávka nebo vratka.

    - **Datum nároku** - Vyberte datum nároku. Výchozí hodnotou je aktuální datum.
    - **Důvod nároku** – Vyberte kód důvodu, který platí pro aktuální odpočet. Vybraný základ nároku ovlivňuje možnosti, které platí. Další informace o tom, jak vytvořit a nakonfigurovat důvody nároku, které jsou zde k dispozici pro výběr, najdete v oddíle [Vytvořte důvody pro odpočet](#deduction-reasons) dříve v tomto tématu.
    - **Poznámky** – Přidejte poznámky, které platí. Po schválení nároku bude moci schvalovatel upravit nebo přidat poznámky k nároku.
    - **Vytvořit deník nároků** – Nastavením této možnosti určíte, zda má být zápis do deník nároků vytvořen při vytvoření nároku nebo odpočtu:

        - *Ano* – Systém vytvoří a zaúčtuje hlavní deník pomocí deníku nároku, který je nastaven na stránce **Parametry pohledávek**. (Další informace najdete v oddíle [Konfigurace pohledávek a odpočtů](#accounts-receivable-deductions) dříve v tomto tématu.) Je-li k reklamaci připojena faktura, použije se deník nároku ke snížení zůstatku příslušné faktury. Pokud bude nárok později zamítnut, budou deník nároku a vypořádání (pokud byla přiložena faktura) stornovány.
        - *Ne* – V tuto chvíli není vytvořen žádný deník nároků. Bude vytvořen po schválení nároku. K novému nároku lze stále připojit fakturu, přestože deník nároku není vytvořen. Vypořádání však nelze provést bez deníku nároků.

1. Vyberte **OK**.

    Je vytvořen nový odpočet. Pokud nastavíte možnost **Vytvořit deník nároků** na *Ano*, jsou zaúčtovány následující transakce:

    - **Dvě nové zákaznické transakce** – Jedna transakce vyrovnává částku nároku vůči původní faktuře. Druhá transakce registruje dluh zákazníka do částky nároku, protože nárok ještě nebyl schválen. Transakce původní faktury a transakce vyrovnávající nárok budou automaticky označeny k vypořádání, když připojíte fakturu výběrem příkazu **Udržovat \> Připojit fakturu** v podokně akcí.
    - **Dvě vyrovnávací transakce** – Tyto transakce jsou zaúčtovány na účet hlavní knihy **Protiúčet odpočtu** .
    - **Deník nároku** – Chcete-li zobrazit deník nároku pro každý odpočet, který je zobrazen na pracovní ploše odpočtu, vyberte kartu **Reference**. Deník nároku je zobrazen v poli **Číslo dávky deníku**. Deník nároku můžete také zobrazit na kartě **Události odpočtu**. Tam bude mít **Typ aktualizace** hodnotu *Shoda*.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Vytvoření odpočtu z vypořádání zákazníka

Proces vytváření odpočtu z vypořádání zákazníka se podobá procesu vytváření odpočtu prostřednictvím pracovní plochy odpočtu. Zákazník a měna faktury jsou však nastaveny automaticky a faktura je přiložena. Při vytváření nároku nebo odpočtu prostřednictvím stránky vypořádání zákazníka nemusíte vybírat příkaz **Udržovat \> Připojit fakturu** v podokně akcí.

1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
1. Vyberte zákazníka, pro kterého chcete vytvořit odpočet.
1. V podokně akcí na kartě **Shromáždit** ve skupině **Vyrovnat** vyberte příkaz **Vyrovnat transakce**.
1. V dialogovém okně **Nastavení transakcí** na kartě **Přehled** vyberte fakturu, vůči které chcete vytvořit odpočet.
1. Na panelu nástrojů vyberte **Srážky \> Nový odpočet**.

    V dialogovém okně **Nový odpočet** je pole **ID odpočtu** nastaveno na základě číselné řady **ID odpočtu**, která je definována na stránce **Parametry správy obchodních náhrad** (**Prodej a marketing \> Nastavení \> Obchodní náhrady \> Parametry správy obchodních náhrad**). Pole **Zákaznický účet** se nastaví na účet zákazníka, na kterého se odpočet vztahuje.

1. Nastavte následující pole:

    - **Externí číslo nároku** – Zadejte referenci nároku od zákazníka.
    - **Částka nároku** – Zadejte částku nároku zahrnující daň. Hodnota musí být kladná.
    - **Měna** – Vyberte měnu pro odpočet. Výchozí hodnota je měna, která je nastavena pro vybraný zákaznický účet.
    - **Základ nároku** – Vyberte základ nároku. Základ nároku určuje typ kreditní transakce, která je vytvořena po schválení odpočtu nebo nároku.

        - *Na základě ceny* – Bude vytvořen návrh faktury s volným textem.
        - *Na základě množství* – Vytvoří se záporná prodejní objednávka nebo vratka.

    - **Datum nároku** - Vyberte datum nároku. Výchozí hodnotou je aktuální datum.
    - **Důvod nároku** – Vyberte kód důvodu, který platí pro aktuální odpočet. Vybraný základ nároku ovlivňuje možnosti, které platí. Další informace o tom, jak vytvořit a nakonfigurovat důvody nároku, které jsou zde k dispozici pro výběr, najdete v oddíle [Vytvořte důvody pro odpočet](#deduction-reasons) dříve v tomto tématu.
    - **Poznámky** – Přidejte poznámky, které platí. Po schválení nároku bude moci schvalovatel upravit nebo přidat poznámky k nároku.
    - **Vytvořit deník nároků** – Nastavením této možnosti určíte, zda má být zápis do deník nároků vytvořen při vytvoření nároku nebo odpočtu:

        - *Ano* – Systém vytvoří a zaúčtuje hlavní deník pomocí deníku nároku, který je nastaven na stránce **Parametry pohledávek**. (Další informace najdete v oddíle [Konfigurace pohledávek a odpočtů](#accounts-receivable-deductions) dříve v tomto tématu.) Je-li k reklamaci připojena faktura, použije se deník nároku ke snížení zůstatku příslušné faktury. Pokud bude nárok později zamítnut, budou deník nároku a vypořádání (pokud byla přiložena faktura) stornovány.
        - *Ne* – V tuto chvíli není vytvořen žádný deník nároků. Bude vytvořen po schválení nároku. K novému nároku lze stále připojit fakturu, přestože deník nároku není vytvořen. Vypořádání však nelze provést bez deníku nároků.

1. Vyberte **OK**.

    Je vytvořen nový odpočet. Pokud nastavíte možnost **Vytvořit deník nároků** na *Ano*, jsou zaúčtovány následující transakce:

    - **Dvě nové zákaznické transakce** – Jedna transakce vyrovnává částku nároku vůči původní faktuře. Druhá transakce registruje dluh zákazníka do částky nároku, protože nárok ještě nebyl schválen. Transakce původní faktury a transakce vyrovnávající nárok budou automaticky označeny k vypořádání, když připojíte fakturu výběrem příkazu **Udržovat \> Připojit fakturu** v podokně akcí.
    - **Dvě vyrovnávací transakce** – Tyto transakce jsou zaúčtovány na účet hlavní knihy **Protiúčet odpočtu** .
    - **Deník nároku** – Chcete-li zobrazit deník nároku pro každý odpočet, který je zobrazen na pracovní ploše odpočtu, vyberte kartu **Reference**. Deník nároku je zobrazen v poli **Číslo dávky deníku**. Deník nároku můžete také zobrazit na kartě **Události odpočtu**. Tam bude mít **Typ aktualizace** hodnotu *Shoda*.

    Vrátíte se na stránku **Vyrovnat transakce**, která nyní zobrazuje vybranou fakturu jako označenou. Tlačítko **Zaúčtovat** je k dispozici, pouze pokud nastavíte možnost **Vytvořit deník nároků** na *Ano*. Pokud je k dispozici, vyberte příkaz **Zaúčtovat** a snižte tak zůstatek na faktuře o hodnotu **Částka nároku**.

### <a name="create-a-deduction-from-a-customer-page"></a>Vytvoření odpočtu ze stránky zákazníka

Proces vytváření odpočtu ze stránky zákazníka se podobá procesu vytváření odpočtu prostřednictvím pracovní plochy odpočtu. Zákazník je však nastaven automaticky.

1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
1. Vyberte zákazníka, pro kterého chcete vytvořit odpočet.
1. V podokně akcí na kartě **Shromáždit** ve skupině **Srážky** vyberte příkaz **Vytvořit odpočty**.

    V dialogovém okně **Nový odpočet** je pole **ID odpočtu** nastaveno na základě číselné řady **ID odpočtu**, která je definována na stránce **Parametry správy obchodních náhrad** (**Prodej a marketing \> Nastavení \> Obchodní náhrady \> Parametry správy obchodních náhrad**). Pole **Zákaznický účet** se nastaví na účet zákazníka, na kterého se odpočet vztahuje.

1. Nastavte následující pole:

    - **Externí číslo nároku** – Zadejte referenci nároku od zákazníka.
    - **Částka nároku** – Zadejte částku nároku zahrnující daň. Hodnota musí být kladná.
    - **Měna** – Vyberte měnu pro odpočet. Výchozí hodnota je měna, která je nastavena pro vybraný zákaznický účet.
    - **Základ nároku** – Vyberte základ nároku. Základ nároku určuje typ kreditní transakce, která je vytvořena po schválení odpočtu nebo nároku.

        - *Na základě ceny* – Bude vytvořen návrh faktury s volným textem.
        - *Na základě množství* – Vytvoří se záporná prodejní objednávka nebo vratka.

    - **Datum nároku** - Vyberte datum nároku. Výchozí hodnotou je aktuální datum.
    - **Důvod nároku** – Vyberte kód důvodu, který platí pro aktuální odpočet. Vybraný základ nároku ovlivňuje možnosti, které platí. Další informace o tom, jak vytvořit a nakonfigurovat důvody nároku, které jsou zde k dispozici pro výběr, najdete v oddíle [Vytvořte důvody pro odpočet](#deduction-reasons) dříve v tomto tématu.
    - **Poznámky** – Přidejte poznámky, které platí. Po schválení nároku bude moci schvalovatel upravit nebo přidat poznámky k nároku.
    - **Vytvořit deník nároků** – Nastavením této možnosti určíte, zda má být zápis do deník nároků vytvořen při vytvoření nároku nebo odpočtu:

        - *Ano* – Systém vytvoří a zaúčtuje hlavní deník pomocí deníku nároku, který je nastaven na stránce **Parametry pohledávek**. (Další informace najdete v oddíle [Konfigurace pohledávek a odpočtů](#accounts-receivable-deductions) dříve v tomto tématu.) Je-li k reklamaci připojena faktura, použije se deník nároku ke snížení zůstatku příslušné faktury. Pokud bude nárok později zamítnut, budou deník nároku a vypořádání (pokud byla přiložena faktura) stornovány.
        - *Ne* – V tuto chvíli není vytvořen žádný deník nároků. Bude vytvořen po schválení nároku. K novému nároku lze stále připojit fakturu, přestože deník nároku není vytvořen. Vypořádání však nelze provést bez deníku nároků.

1. Vyberte **OK**.

    Je vytvořen nový odpočet. Pokud nastavíte možnost **Vytvořit deník nároků** na *Ano*, jsou zaúčtovány následující transakce:

    - **Dvě nové zákaznické transakce** – Jedna transakce vyrovnává částku nároku vůči původní faktuře. Druhá transakce registruje dluh zákazníka do částky nároku, protože nárok ještě nebyl schválen. Transakce původní faktury a transakce vyrovnávající nárok budou automaticky označeny k vypořádání, když připojíte fakturu výběrem příkazu **Udržovat \> Připojit fakturu** v podokně akcí.
    - **Dvě vyrovnávací transakce** – Tyto transakce jsou zaúčtovány na účet hlavní knihy **Protiúčet odpočtu** .
    - **Deník nároku** – Chcete-li zobrazit deník nároku pro každý odpočet, který je zobrazen na pracovní ploše odpočtu, vyberte kartu **Reference**. Deník nároku je zobrazen v poli **Číslo dávky deníku**. Deník nároku můžete také zobrazit na kartě **Události odpočtu**. Tam bude mít **Typ aktualizace** hodnotu *Shoda*.

## <a name="create-a-credit-note-for-a-customer"></a>Vytvoření dobropisu pro zákazníka

Pokud existuje schválený rabat pro zákazníka, vytvořte dobropis na účet zákazníka představující rabat. Kredit se pak zobrazí v pracovní ploše odpočtu, kde lze spárovat se srážkou.

Dobropis vytvoříte takto.

1. Přejděte na **Prodej a marketing \> Odběratelé \> Všichni odběratelé**.
1. Vyberte zákazníka.
1. V podokně akcí na kartě **Shromáždit** ve skupině **Vyrovnat** vyberte příkaz **Vyrovnat transakce**.
1. V dialogovém okně **Vyrovnat transakce** vyberte transakci, na kterou byl rabat použit.
1. Na panelu nástrojů vyberte v nabídce **Funkce** typ rabatového programu, který platí.
1. Na stránce **Rabat** vyberte na kartě **Přehled** zaškrtávací políčko **Označit** vedle ID příslušného rabatu.
1. V podokně akcí vyberte **Funkce \> Vytvořit dobropis**.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Zpracování odpočtu na pracovní ploše odpočtu

Ke spárování odpočtů s otevřenými kreditními transakcemi, rozdělení srážek, zamítnutí srážek a odpisu odpočtů můžete použít pracovní plochu odpočtu.

V závislosti na tom, jakým způsobem chcete zpracovat odpočet, proveďte jednu nebo více procedur v následujících dílčích oddílech: Postupy můžete podle potřeby kombinovat. Můžete například rozdělit odpočet na dvě části a potom spárovat jednu část ke kreditu, ale ponechat zbývající část v pracovní ploše pro spárování s jiným kreditem později. Můžete také lze spárovat odpočet s kreditem, který je menší než částka odpočtu, a poté zamítnout nebo odepsat zbývající zůstatek odpočtu.

### <a name="match-a-deduction-to-a-credit"></a>Spárování odpočtu s kreditem

Chcete-li spárovat odpočet s kreditem, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. Zaškrtněte políčko **Označit** vedle odpočtu, který má být zpracován.
1. V oddíle **Otevřené transakce** vyberte zaškrtávací políčko **Označit** u kreditu, který se má spárovat s odpočtem. Pokud je uvedeno více kreditů, můžete ke spárování s odpočtem vybrat více než jeden kredit. Pokud chcete, aby systém automaticky vybral kredity, které odpovídají částce odpočtu, vyberte na panelu nástrojů příslušnou možnost v nabídce **Vybrat částku odpočtu**.
1. V podokně akcí vyberte položku **Udržovat \> Spárovat**. Systém spáruje odpočet s kreditem. Pokud zůstatek zůstane v odpočtu, zobrazí se v poli **Zbývající množství** na kartě **Srážky**.

    > [!NOTE]
    > U odpočtů, které byly vytvořeny pomocí příkazu **Nový odpočet** na pracovní ploše odpočtu, ve vypořádání zákazníka nebo na stránce zákazníka, je příkaz **Udržovat \> Spárovat** k dispozici, pouze pokud je pole **Stav nároku** nastaveno na *Přijato*. Tento příkaz lze použít k ručnímu spárování transakce založené na ceně nebo množství k přidruženému kreditu v oddíle **Otevřené transakce**. Tento kredit se vytvoří buď při schválení odpočtu (pomocí příkazu **Udržovat \> Schválit odpočet**), nebo když je připojen ke stávajícímu kreditu, jak je popsáno v oddíle [Kredity vytvořené mimo schvalovací proces odpočtu](#credits-outside-approval) dále v tomto tématu. Periodický úkol *Vypořádat schválené odpočty* (**Prodej a marketing \> Periodické úkoly \> Vypořádat schválené odpočty**) lze také použít k automatickému spárování odpočtů a kreditů, které mají shodné hodnoty **ID odpočtu** a částky.

### <a name="split-a-deduction"></a>Rozdělení odpočtu

Chcete-li rozdělit odpočet, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. Zaškrtněte políčko **Označit** vedle odpočtu, který má být zpracován.
1. V podokně akcí vyberte položku **Udržovat \> Rozdělit**.
1. V dialogovém okně **Rozdělit** zapište do pole **Rozdělit částku** částku, kterou chcete oddělit od hlavního odpočtu. Pak vyberte **OK**.
1. Na kartě **Odpočty** si všimněte nového záznamu částky rozdělení. Původní záznam odpočtu obsahuje připomínku zůstatku odpočtu. Nyní můžete obě části původního rabatu spravovat odděleně.
1. Vyberte záznam původního odpočtu a poté vyberte kartu **Reference**. Pole **Rozdělit částku** zobrazuje částku, která byla odtržena od původní částky.

### <a name="attach-an-invoice-to-a-deduction"></a>Připojení faktury k odpočtu

K odpočtu můžete připojit fakturu, pokud byl odpočet vytvořen pomocí příkazu **Nový odpočet** na pracovní ploše odpočtu, ve vypořádání zákazníka nebo na stránce zákazníka, a pokud k němu aktuálně není připojena faktura (tj. sloupec **Faktura** je prázdný).

Chcete-li připojit fakturu k odpočtu, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. Zaškrtněte políčko **Označit** vedle odpočtu, který má být zpracován.
1. V podokně akcí zvolte **Udržovat \> Připojit fakturu**.
1. V dialogovém okně **Přiložit fakturu** vyberte fakturu a poté vyberte **OK**.
1. V dialogovém okně **Vypořádat transakce** postupujte podle jednoho z těchto kroků, v závislosti na tom, zda byl při vytváření odpočtu zaúčtován deník nároku:

    - Pokud byl deník nároku zaúčtován, vybraná faktura a transakce zákaznického kreditu deníku nároku zobrazí značku zaškrtnutí ve sloupci **Označit**. Zvolte **Zaúčtovat**. Zbývající zůstatek na přiložené faktuře je snížen o částku nároku.
    - Pokud nebyl deník nároku zaúčtován, žádná transakce u sebe nemá značku zaškrtnutí ve sloupci **Označit**. Protože nemůžete účtovat protiúčtem vůči deníku nároku, dokud není odpočet schválen, vyberte příkaz **Zrušit**.

### <a name="detach-an-invoice-from-a-deduction"></a>Odpojení faktury od odpočtu

Od odpočtu můžete odpojit fakturu, pokud byl odpočet vytvořen pomocí příkazu **Nový odpočet** na pracovní ploše odpočtu, ve vypořádání zákazníka nebo na stránce zákazníka, a pokud k němu aktuálně je připojena faktura (tj. sloupec **Faktura** je zobrazuje číslo faktury) a sloupec **Stav nároku** je nastaven na *Otevřeno*. Tento úkol možná dokončíte, protože byla přiložena nesprávná faktura. Faktura je odebrána z odpočtu a její zbývající zůstatek se aktualizuje, pokud byl snížen při přiložení faktury.

Pokud chcete odpojit fakturu, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. Zaškrtněte políčko **Označit** vedle odpočtu, který má být zpracován.
1. V podokně akcí zvolte **Udržovat \> Odpojit fakturu**.

### <a name="approve-a-deduction"></a>Schválení odpočtu

Schválit můžete odpočty, které byly vytvořeny pomocí příkazu **Nový odpočet** na pracovní ploše odpočtu, ve vypořádání zákazníka nebo na stránce zákazníka. Odpočty však můžete schválit pouze když je pole **Stav nároku** nastaveno na *Otevřeno*.

Chcete-li schválit odpočet, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. Zaškrtněte políčko **Označit** vedle odpočtu, který má být zpracován.
1. V podokně akcí zvolte **Udržovat \> Schválit odpočet**.
1. V dialogovém okně **Schválit odpočet** upravte nebo přidejte informace do pole **Poznámka** podle potřeby.
1. Pokud je odpočet založen na ceně a nebyla k němu připojena faktura, vyberte skupinu DPH položky. Skupina DPH položky je obvykle nastavena ve faktuře. Pokud tedy není kód DPH připojen k faktuře, musí být uveden.
1. Vyberte **OK**.

    V tuto chvíli již nelze v odpočtu provádět žádné další změny. Pokud byla při vytvoření odpočtu možnost **Vytvořit deník nároku** nastavena na *Ne*, je deník nároku vytvořen a zaúčtován po schválení odpočtu. Po schválení odpočtu se automaticky vytvoří a otevře kredit. Typ závisí na hodnotě **Základ nároku** odpočtu:

    - *Na základě ceny* – Pokud je odpočet založen na ceně, je pro zákaznický účet vytvořena faktura s volným textem. Můžete přidat popis a kredit zaúčtovat. Při vytváření konceptu jsou odpočtem vyplněna následující pole:

        - **ID odpočtu** – Toto pole je přidáno do záhlaví, aby byla umožněna sledovatelnost zpět k odpočtu.
        - **Hlavní účet** – Hodnota je určena polem **Účet pro zaúčtování nároku**, které je nastaveno pro důvod odpočtu přiřazený k odpočtu.
        - **Skupina DPH položky** – Hodnota je určena přiloženou fakturou nebo hodnotou, kterou jste vybrali při schválení odpočtu.
        - **Jednotková cena** – Hodnota je připsána částkou nároku na odpočet.
        - **Text faktury** – Ve výchozím nastavení je toto pole nastaveno na hodnotu **Poznámky** odpočtu.

    - *Na základě množství* – Pokud je odpočet založen na množství, vytvoří se otevřená prodejní objednávka nebo vratka. Nastavení **Vytvořit vratku** na stránce **[Parametry pohledávek](#accounts-receivable-deductions)** určuje, zda se při schválení odpočtu vytvoří prodejní objednávka nebo vratka. Zobrazí se stránka **Kopírovat objednávky**, která je filtrována tak, aby zobrazovala řádky, kde je pole **Účet faktury** nastaveno na zákaznický účet odpočtu. Postupujte následovně:

        1. Na záložce **Faktury** ukazuje oddíl **Záhlaví** prodejní faktury, kde **Účet faktury** odpovídá zákaznickému účtu odpočtu. Vyberte příslušnou prodejní fakturu.
        1. Oddíl **Řádky** zobrazuje řádky z vybrané prodejní faktury. Zaškrtněte políčko **Vybrat** pro každý řádek, který chcete kopírovat. Případně v oddíle **Záhlaví** vyberte zaškrtávací políčko **Vybrat vše** u prodejní objednávky a tak vyberte všechny její řádky.
        1. Upravte **Množství** u jednoho nebo více řádků podle potřeby.

            Všechny řádky, které jste dosud vybrali, jsou uvedeny na záložce **Vybrané řádky nebo záhlaví ke zkopírování**.

        1. Předchozí dva kroky opakujte podle potřeby, dokud nejsou na záložce **Vybrané řádky nebo záhlaví ke zkopírování** uvedeny všechny požadované řádky.
        1. Vyberte **OK**.

            Otevře se nová vratka a automaticky se nastaví následující pole:

            - **ID odpočtu** – Toto pole je přidáno do záhlaví, aby byla umožněna sledovatelnost zpět k odpočtu.
            - **Kód důvodu vrácení** – Ve výchozím nastavení je toto pole nastaveno na hodnotu **Kódu důvodu vrácení** pro důvod odpočtu, který je přiřazen k odpočtu.

Jakmile je kredit fakturován, zobrazí se v části **Otevřené transakce** pracovní plochy odpočtu oproti příslušné hodnotě **ID odpočtu**, a jeho pole **Typ nároku** je nastaveno na *Jiné kredity*. Kredit bude k dispozici, dokud nebude jedním z následujících způsobů vyrovnán s odpočtem:

- Ruční vypořádání provedete výběrem nabídky **Udržovat \> Spárovat** v podokně akcí.
- Automatické vypořádání provede periodický úkol *Vypořádat schválené nároky* (**Prodej a marketing \> Periodické úkoly \>Vypořádat schválené nároky**).
- Je to automaticky vypořádáno, protože možnost **Automatické vypořádání** na kartě **Vypořádání** stránky **Parametry pohledávek** je nastavena na *Ano*.

Chcete-li zobrazit kredit, který je vytvořen při schválení odpočtu, můžete také použít tlačítko **Otevřený kredit** v oddíle **Otevřené transakce** pracovní plochy odpočtu.

### <a name="create-a-return-order"></a>Vytvořit vratku

Pro odpočty, které byly vytvořeny pomocí příkazu **Nový odpočet** na pracovní ploše odpočtu, ve vypořádání zákazníka nebo na stránce zákazníka, můžete vytvořit vratku. Musí však být splněny všechny následující podmínky:

- Pole **Základ nároku** je nastaveno na hodnotu *Na základě množství*.
- Pole **Stav nároku** je nastaveno na *Otevřeno*.
- Možnost **Vytvořit vratku** na kartě **Srážky** stránky **[Parametry pohledávek](#accounts-receivable-deductions)** je nastavena na *Ano*.
- Možnost **Před schválením odpočtu vytvořit vratku** na kartě **Srážky** stránky **[Parametry pohledávek](#accounts-receivable-deductions)** je nastavena na *Ano*.

Chcete-li vytvořit vratku, postupujte následujícím způsobem.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. Zaškrtněte políčko **Označit** vedle odpočtu, který má být zpracován.
1. V podokně Akce vyberte možnost **Udržovat \> Vytvořit vratku**.
1. V dialogovém okně **Schválit odpočet** upravte nebo přidejte informace do stávající hodnoty pole **Poznámka** podle potřeby, a poté vyberte **OK**.
1. Na záložce **Faktury** v dialogovém okně **Kopírovat objednávky** ukazuje oddíl **Záhlaví** prodejní faktury, kde **Účet faktury** odpovídá zákaznickému účtu odpočtu. Vyberte příslušnou prodejní fakturu.
1. Oddíl **Řádky** zobrazuje řádky z vybrané prodejní faktury. Zaškrtněte políčko **Vybrat** pro každý řádek, který chcete kopírovat. Případně v oddíle **Záhlaví** vyberte zaškrtávací políčko **Vybrat vše** u prodejní objednávky a tak vyberte všechny její řádky.
1. Upravte **Množství** u jednoho nebo více řádků podle potřeby.

    Všechny řádky, které jste dosud vybrali, jsou uvedeny na záložce **Vybrané řádky nebo záhlaví ke zkopírování**.

1. Předchozí dva kroky opakujte podle potřeby, dokud nejsou na záložce **Vybrané řádky nebo záhlaví ke zkopírování** uvedeny všechny požadované řádky.
1. Vyberte **OK**.

    Otevře se nová vratka a automaticky se nastaví následující pole:

    - **ID odpočtu** – Toto pole je přidáno do záhlaví, aby byla umožněna sledovatelnost zpět k odpočtu.
    - **Kód důvodu vrácení** – Ve výchozím nastavení je toto pole nastaveno na hodnotu **Kódu důvodu vrácení** pro důvod odpočtu, který je přiřazen k odpočtu.

### <a name="deny-a-deduction"></a>Odmítnutí odpočtu

Chcete-li odmítnout odpočet, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. Zaškrtněte políčko **Označit** vedle odpočtu, který má být zpracován.
1. V podokně akcí vyberte položku **Udržovat \> Odmítnout**.
1. V dialogovém okně **Odmítnout** vyberte kód příčiny zamítnutí a poté vyberte **OK**.
1. V poli **Zobrazit** pod podoknem Akce vyberte *Zavřeno*.

    Zamítnutý odpočet je zobrazen na kartě **Srážky** a pole **Zbývající částka** odpočtu je nastaveno na *0,00*.

    U odpočtů, které byly vytvořeny pomocí příkazu **Nový odpočet** na pracovní ploše odpočtu, ve vypořádání zákazníka nebo na stránce zákazníka, se mohou vyskytnout následující události:

    - Na kartě **Reference** jsou aktualizována pole v oddíle **Odmítnutí**.
    - Pokud jste při vytváření odpočtu vybrali vytvoření deníku nároku a pokud byla k odpočtu přiložena faktura snižující zůstatek na faktuře, faktura se odpojí a zbývající zůstatek dříve připojené faktury se zvýší o částku zamítnutého nároku.
    - Pole **Stav** odpočtu je nastaveno na *Zavřeno*.
    - Pole **Stav nároku** odpočtu je nastaveno na *Odmítnuto*.

Chcete-li stornovat zamítnutí, postupujte takto.

1. Na kartě **Srážky** vyberte zamítnutý odpočet.
1. V podokně Akce klikněte na možnost **Stornovat zamítnutí**.

    U odpočtů, které byly vytvořeny pomocí příkazu **Nový odpočet** na pracovní ploše odpočtu, ve vypořádání zákazníka nebo na stránce zákazníka, se mohou vyskytnout následující události:

    - Na kartě **Reference** jsou aktualizována pole v oddíle **Odmítnutí**.
    - Pole **Stav** odpočtu je nastaveno na *Otevřeno*.
    - Pole **Stav nároku** odpočtu je nastaveno na *Otevřeno*.

### <a name="write-off-a-deduction"></a>Odepsání odpočtu

Chcete-li odepsat odpočet, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. Zaškrtněte políčko **Označit** vedle odpočtu, který má být zpracován.
1. V podokně akcí vyberte položku **Udržovat \> Odpis**.
1. V dialogovém okně **Odpis** vyberte kód příčiny odepsání a poté vyberte **OK**.
1. V poli **Zobrazit** vyberte *Uzavřeno*.

    Odepsaný odpočet je zobrazen na kartě **Srážky** a pole **Zbývající částka** odpočtu je nastaveno na *0,00*.

    U odpočtů, které byly vytvořeny pomocí příkazu **Nový odpočet** na pracovní ploše odpočtu, ve vypořádání zákazníka nebo na stránce zákazníka, se mohou vyskytnout následující události:

    - Na kartě **Reference** jsou aktualizována pole v oddíle **Odpis**.
    - Pokud jste deník nároku vytvořili v době, kdy byl vytvořen odpočet, je deník nároku zaúčtován na kód důvodu odpisu odpočtu. Tuto položku můžete zobrazit na kartě **Události odpočtu**, kde její pole **Typ aktualizace** má hodnotu *Odpis*.
    - Pole **Stav** odpočtu je nastaveno na *Zavřeno*
    - Pole **Stav nároku** odpočtu je nastaveno na *Odpis*.

Chcete-li stornovat odpis, postupujte takto.

1. Na kartě **Srážky** vyberte zamítnutý odpočet.
1. V podokně akcí vyberte položku **Stornovat odpis**.

    U odpočtů, které byly vytvořeny pomocí příkazu **Nový odpočet** na pracovní ploše odpočtu, ve vypořádání zákazníka nebo na stránce zákazníka, se mohou vyskytnout následující události:

    - Na kartě **Reference** jsou aktualizována pole v oddíle **Odpis**.
    - Pokud jste deník nároku vytvořili v době, kdy byl vytvořen odpočet, je deník nároku zaúčtován na kód důvodu odpisu odpočtu. Tuto položku můžete zobrazit na kartě **Události odpočtu**, kde její pole **Typ aktualizace** má hodnotu *Stornovat odpis*.
    - Pole **Stav** odpočtu je nastaveno na *Otevřeno*.
    - Pole **Stav nároku** odpočtu je nastaveno na *Otevřeno*.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Kredity vytvořené mimo schvalovací proces odpočtu

Tato část platí pouze pro odpočty, které byly vytvořeny pomocí příkazu **Nový odpočet** na pracovní ploše odpočtu, ve vypořádání zákazníka nebo na stránce zákazníka.

Jiní uživatelé již mohli vytvořit bezplatnou textovou fakturu, vratku nebo zápornou prodejní objednávku pro nárok zákazníka mimo proces **Schválit odpočet**. Když je stávající odpočet schválen na pracovní ploše odpočtu, systém automaticky vytvoří další fakturu s volným textem, vratku nebo zápornou prodejní objednávku. Tato část popisuje, jak připojit stávající kredity k odpočtu před jeho schválením, aby se předešlo duplicitním kreditům.

### <a name="attach-a-credit-to-deduction"></a>Připojení kreditu k odpočtu

Tato část popisuje, jak lze k odpočtu z kreditu připojit kredit.

Po připojení kreditu k odpočtu můžete kredit zobrazit pomocí tlačítka **Otevřený kredit** na panelu nástrojů v oddíle **Otevřené transakce** pracovní plochy odpočtu.

Jakmile je kredit fakturován a odpočet je schválen, zobrazí se kredit v části **Otevřené transakce** pracovní plochy odpočtu oproti příslušné hodnotě **ID odpočtu**, a jeho pole **Typ nároku** je nastaveno na *Jiné kredity*.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Připojení faktury s volným textem k odpočtu

Chcete-li k odpočtu připojit fakturu s volným textem, postupujte takto.

1. Přejděte na **Pohledávky \> Faktury \> Všechny volné faktury**.
1. Vyberte příslušnou fakturu.
1. V podokně akcí na kartě **Faktura** zvolte příkaz **Připojit kredit k odpočtu**. Toto tlačítko je k dispozici pouze, je-li pole **ID odpočtu** faktury s volným textem prázdné. Prázdné pole označuje, že faktura s volným textem již není připojena k odpočtu.
1. Na stránce **Připojit kredit k odpočtu** můžete vybrat *jeden* odpočet. Vybrat je možné pouze otevřené odpočty *na základě ceny*.
1. Vyberte **OK**. Pole **ID odpočtu** je nastaveno v záhlaví faktury s volným textem.

#### <a name="attach-a-return-order-to-a-deduction"></a>Připojení vratky k odpočtu

Chcete-li připojit vratku k odpočtu, postupujte takto.

1. Přejděte na **Pohledávky \> Objednávky \> Všechny vratky**.
1. Vyberte příslušné číslo přijaté nebo otevřené autorizace vrácení zboží (RMA).
1. V podokně akcí na kartě **Vratka** zvolte příkaz **Připojit kredit k odpočtu**. Toto tlačítko je k dispozici pouze, je-li pole **ID odpočtu** vratky prázdné. Prázdné pole označuje, že vratka již není připojena k odpočtu.
1. Na stránce **Připojit kredit k odpočtu** můžete vybrat *jeden* odpočet. Vybrat je možné pouze otevřené odpočty *na základě množství*.
1. Vyberte **OK**. Pole **ID odpočtu** je nastaveno v záhlaví vratky.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Připojení prodejní objednávky k odpočtu

Chcete-li připojit prodejní objednávku k odpočtu, postupujte takto.

1. Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky**.
1. Vyberte příslušnou otevřenou, dodanou nebo fakturovanou prodejní objednávku.
1. V podokně akcí na kartě **Faktura** zvolte příkaz **Připojit kredit k odpočtu**. Toto tlačítko je k dispozici pouze, je-li pole **ID odpočtu** prodejní objednávky prázdné. Prázdné pole označuje, že prodejní objednávka již není připojena k odpočtu.
1. Na stránce **Připojit odpočet** můžete vybrat *jeden* odpočet. Vybrat je možné pouze otevřené odpočty *na základě množství*.
1. Vyberte **OK**. Pole **ID odpočtu** je nastaveno v záhlaví prodejní objednávky.

#### <a name="detach-a-deduction-from-a-credit"></a>Odpojení odpočtu od kreditu

Pokud byl připojen nesprávný odpočet, můžete jej od kreditu odpojit. Musí však být splněny všechny následující podmínky:

- K odpočtu je připojen kredit.
- Pole **Stav nároku** je nastaveno na *Otevřeno*.

Chcete-li odpojit odpočet od kreditu, postupujte podle jednoho z těchto kroků v závislosti na typu kreditu:

- **Volné faktury**: Na stránce **Všechny volné faktury** vyberte fakturu. Poté v podokně akcí na kartě **Faktura** zvolte příkaz **Odpojit kredit od odpočtu**.
- **Vratky:** Na stránce **Všechny vratky** vyberte vratku. Poté v podokně akcí na kartě **Vratka** zvolte příkaz **Odpojit kredit od odpočtu**.
- **Prodejní objednávky:** Na stránce **Všechny prodejní objednávky** vyberte objednávku. Poté v podokně akcí na kartě **Faktura** zvolte příkaz **Odpojit kredit od odpočtu**.

### <a name="attach-a-deduction-to-a-credit"></a>Připojení odpočtu ke kreditu

Tato část popisuje, jak lze připojit odpočet ke kreditu z odpočtu.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Připojení odpočtu ke kreditu volné faktury, vratky nebo prodejní objednávky

Chcete-li připojit odpočet ke kreditu volné faktury, vratky nebo prodejní objednávky, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. Vyberte příslušný otevřený odpočet.
1. V podokně akcí zvolte **Udržovat \> Připojit odpočet ke kreditu**. Toto tlačítko je k dispozici pouze v případě, kdy je pole **Stav nároku** nastaveno na *Otevřeno*.
1. Na stránce **Připojit kredit** můžete vybrat *jeden* kredit. Typ zobrazených kreditů závisí na hodnotě odpočtu **Základ nároku**:

    - *Na základě ceny* - Stránka zobrazuje faktury s volným textem pro zákaznický účet, kde je pole **ID odpočtu** prázdné. Zobrazují se také požadavky zákazníků, protože faktura s volným textem může být nezaúčtována. Proto nemusí mít číslo, na které lze odkazovat.
    - *Na základě množství* - Typ zobrazených kreditů závisí na nastavení možnosti **Vytvořit vratku** na stránce **[Parametry pohledávek](#accounts-receivable-deductions)**:

        - *Ano* - Stránka zobrazuje vratky pro zákaznický účet, kde je pole **ID odpočtu** prázdné.
        - *Ne* - Stránka zobrazuje prodejní objednávky pro zákaznický účet, kde je pole **ID odpočtu** prázdné.

1. Vyberte **OK**. Pole **ID odpočtu** je nastaveno v záhlaví kreditu.

Po připojení kreditu k odpočtu můžete kredit zobrazit pomocí tlačítka **Otevřený kredit** na panelu nástrojů v oddíle **Otevřené transakce** pracovní plochy odpočtu.

Jakmile je kredit fakturován a odpočet je schválen, zobrazí se kredit v části **Otevřené transakce** pracovní plochy odpočtu oproti příslušné hodnotě **ID odpočtu**, a jeho pole **Typ nároku** je nastaveno na *Jiné kredity*.

#### <a name="detach-a-credit-from-the-deduction"></a>Odpojení kreditu od odpočtu

Pokud byl připojen nesprávný kredit, můžete jej od odpočtu odpojit. V podokně akcí ve skupině **Udržovat** zvolte příkaz **Odpojit kredit od odpočtu**. Hodnota **ID odpočtu** je z kreditu odstraněna.

Tlačítko **Odpojit odpočet od kreditu** je k dispozici pouze když jsou splněny následující podmínky:

- K odpočtu je připojen kredit.
- Pole **Stav nároku** je nastaveno na *Otevřeno*.

## <a name="create-a-one-time-promotion"></a>Vytvoření jednorázové promoakce

V některých případech jste možná neschválili rabat, který lze spárovat s odpočtem. V takovém případě lze použít funkci *jednorázové promoakce* pro spárování odpočtu s obchodní náhradou, která je spojena s odběratelem. Funkce *jednorázové promoakce* vytvoří novou smlouvu o obchodních náhradách a promoakce s paušální částkou. Funkce pak spáruje paušál s odpočtem a provede zaúčtování, která jsou požadována pro zavření odpočtu.

Tato funkce je užitečná, pokud používáte obchodní náhrady. Další informace o obchodních náhradách najdete v části [Správa obchodních náhrad](../sales-marketing/trade-allowance.md).

Nejprve musíte nastavit šablonu, kterou lze použít k vytvoření nové smlouvy o obchodní náhradě. Chcete-li nastavit šablonu, postupujte následujícím způsobem.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Šablony**.
1. V podokně akcí zvolte **Nový**.
1. Do polí zadejte informace, které se mají objevit na smlouvách, které jsou vytvořeny z šablony.
1. Na záložce **Zákazníci** vyberte v poli **Hierarchie** úroveň hierarchie.
1. V seznamu hierarchie vyberte zákazníka, který má nespárovaný odpočet, a poté vyberte tlačítko se šipkou doprava (**\>**). Zákazník je přidán do seznamu **Zákazníci s dohodou o obchodních náhradách**.
1. Nastavte zbývající pole podle potřeby a poté zavřete stránku.
1. Přejděte do nabídky **Prodej a marketing \> Nastavení \> Obchodní náhrady \> Parametry správy obchodních náhrad**.
1. Na kartě **Přehled** vyberte v poli **Šablona jednorázové promoakce** název šablony, kterou chcete použít k vytvoření jednorázových promoakcí.

Dále můžete vytvořit jednorázovou promoakci v pracovní ploše odpočtu. Chcete-li vytvořit jednorázovou promoakci, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. Zaškrtněte políčko **Označit** vedle odpočtu, který má být zpracován.
1. V podokně akcí vyberte **Udržovat \> Vyrovnat srážku jako jednorázovou promoakci**.
1. V dialogovém okně **Jednorázová promoakce** přiřaďte odpočet k jednomu nebo více finančním prostředkům takto:

    1. Vyberte možnost **Nový** a poté v poli **ID finančních prostředků** vyberte ID finančních prostředků. Zopakujte tento krok pro přidání libovolného počtu finančních prostředků.
    1. V poli **Procento** vedle ID jednotlivých finančních prostředků zadejte procento odpočtu, které se má přidělit k finančním prostředkům. Částky, které zadáte do polí **Procento**, musejí dávat dohromady 100 procent.

1. Vyberte **OK**. Systém vytvoří novou smlouvu o obchodních náhradách s paušální promoakcí a spáruje paušální částku s odpočtem.

## <a name="do-a-mass-update-of-deductions"></a>Provedení hromadné aktualizace odpočtů

Pokud musíte provést stejnou změnu u více odpočtů, lze vybrat tyto odpočty a provést hromadnou aktualizaci jejich polí.

Chcete-li provést hromadnou aktualizaci, postupujte takto.

1. Přejděte do nabídky **Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**.
1. V poli **Zobrazit** pod podoknem Akce vyberte typ odpočtu ke zobrazení.
1. Zaškrtněte políčko u každého odpočtu, který chcete aktualizovat. Poté v podokně akcí zvolte **Udržovat \> Hromadná aktualizace**.
1. Dialogové okno **Hromadná aktualizace** zobrazí vybrané odpočty. Aktualizujte pole podle potřeby a poté tlačítkem **OK** přijměte změny.
