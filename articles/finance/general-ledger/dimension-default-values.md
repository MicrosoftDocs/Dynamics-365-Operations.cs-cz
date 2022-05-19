---
title: Výchozí finanční dimenze ve finančních denících
description: Toto téma popisuje pravidla, která definují, jak se nastavují hodnoty finanční dimenze u transakcí zadávaných prostřednictvím finančních deníků. Obsahuje také podrobnosti pro scénáře, kde se používají pevné dimenze.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 51235b8a5dac50aad5031456760c970e50506d66
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713099"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Výchozí finanční dimenze ve finančních denících

[!include [banner](../includes/banner.md)]

Toto téma popisuje pravidla, která definují, jak se nastavují hodnoty finanční dimenze u transakcí zadávaných prostřednictvím finančních deníků (ale ne prostřednictvím skladových deníků nebo projektových deníků). Obsahuje také podrobnosti pro scénáře, kde se používají pevné dimenze.

## <a name="symptom"></a>Příznak

Hodnoty finanční dimenze nejsou ve finančním deníku nastaveny podle očekávání na účtu nebo offsetovém účtu. Následující scénáře představují dva příklady:

Poukaz se zapisuje do obecného deníku. Účet je účet dodavatele a offsetový účet je bankovní účet. Finanční dimenze dodavatele jsou ve výchozím nastavení zadávány na Účet, ale finanční dimenze banky nejsou ve výchozím nastavení zadávány na ofsetový účet. Namísto toho jsou hodnoty dimenzí z účtu ve výchozím nastavení zadávány na ofsetový účet.

Zákazník má přiřazeny výchozí hodnoty finanční dimenze a hlavní účet výnosů má pro finanční dimenzi oddělení přiřazenou hodnotu pevné dimenze. Poukaz se zapisuje do obecného deníku.  Účet je zákazník a offsetový účet je hlavní kniha, konkrétně výnosový účet s hodnotou pevné dimenze. V účtu Offset pro hlavní výnosový účet není nastavena pevná dimenze. Místo toho je nastavena na hodnotu dimenze oddělení z účtu, který přišel od zákazníka.  Po zaúčtování poukázky je na zaúčtovaném účetním záznamu použita hodnota pevné dimenze, ale na poukázce je stále uvedena hodnota oddělení zákazníka na výnosovém účtu. 

Jaká pravidla se dodržují pro hodnoty finanční dimenze stanovené pro poukázky v deníku?

## <a name="resolution"></a>Řešení

Při zadávání hodnot finanční dimenze ve výchozím nastavení na řádky poukázky ve finančních denících, jako je obecný deník nebo deník faktur dodavatele, se dodržují následující pravidla. 

1. **Hlavička deníku**

   - Dimenze hlavičky deníku se ve výchozím nastavení zadávají z dimenzí názvu deníku.

2. **Účet řádku deníku**

   - Dimenze účtu řádku deníku se ve výchozím nastavení zadávají z dimenzí hlavičky deníku.
   - Pokud jsou jakékoli finanční dimenze prázdné, jejich hodnoty se ve výchozím nastavení zadávají z dimenzí zákazník, dodavatel, banka, dlouhodobý majetek, projekt nebo hlavní kniha.

     - Pokud je typ účtu **hlavní kniha**, s pevnou dimenzí na účtu hlavní knihy se při zadávání transakce zachází jako s výchozí dimenzí.
     - Pokud je typ účtu **zákazník**, **dodavatel**, **banka**, **dlouhodobý majetek**, nebo **projekt**, hlavní účet zatím nelze určit. Pevná dimenze proto pro účet nikdy nebude zadána.

3. **Ofsetový účet řádku deníku**

 - Dimenze ofsetového účtu řádku deníku se ve výchozím nastavení zadávají z dimenzí účtu řádku deníku.

 - Pokud jsou jakékoli finanční dimenze prázdné, další výchozí položka bude pocházet z výchozích dimenzí zákazník, dodavatel, banka, dlouhodobý majetek, projekt nebo hlavní kniha.
   1. Pokud je typ ofsetového účtu **hlavní kniha**, s pevnou dimenzí na účtu hlavní knihy se při zadávání transakce zachází jako s výchozí dimenzí. Pokud byla hodnota dimenze již ve výchozím nastavení zadána z účtu, výchozí nebo pevná hodnota dimenze hlavního účtu nepřepíše stávající hodnotu.
   2. Pokud je typ ofsetového účtu **zákazník**, **prodejce**, **banka**, **dlouhodobý majetek**, nebo **projekt**, hlavní účet ještě není znám, takže pevná dimenze nebude pro ofsetový účet nikdy výchozí.

4. **Zaúčtování**

    1. Během účtování se vyhodnotí hlavní účet pro každý řádek účetního záznamu (pro účet i pro ofsetový účet), aby se určilo, zda existuje hodnota pevné dimenze. Pokud je definována pevná dimenze, všechny stávající nebo prázdné hodnoty budou nahrazeny touto pevnou hodnotou dimenze.

        Hodnota pevné dimenze **není** zobrazena na řádcích deníku po zaúčtování. Místo toho se zobrazí v účetním záznamu při zobrazení poukazu po jeho zaúčtování.

    2. Ve výchozím nastavení nejsou během účtování zadávány žádné jiné hodnoty dimenzí, včetně dalších účtů hlavní knihy, které by mohly být přidány během účtování, jako jsou účty zaokrouhlování penny a mezipodnikové kvůli účtům nebo splatným z účtů. Výchozí položky dimenze pro další účty hlavní knihy jsou převzaty z účtu nebo ofsetového účtu.

Pro účely výchozího nastavení zadávání hodnot dimenze nemůže výchozí proces deníku určit, zda byla prázdná hodnota dimenze záměrně ponechána prázdná, nebo zda nebyl proveden výchozí záznam. Pokud je hodnota dimenze záměrně ponechána prázdná, může být hodnota ve výchozím nastavení zadána pomocí výchozího pořadí, které bylo popsáno dříve. Pokud požadujete, aby dimenze měla prázdnou hodnotu, možná budete muset vytvořit dimenzi, která má hodnotu **0** (nula) nebo **prázdný**, takže jej lze použít místo prázdné dimenze.

Prohlédněte si následující scénáře a podívejte se na příklady výchozího pořadí finanční dimenze.

### <a name="scenario-1"></a>Scénář 1

Jděte do **Hlavní kniha \> Nastavení deníku \> Názvy deníků** a vyberte název deníku **GenJrn**. Poté na záložce s náhledem **Finanční dimenze** definujte následující hodnoty pro výchozí finanční dimenze:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Stránka s názvy deníků](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

Jděte do **Hlavní kniha \> Položky deníku \> Obecný deník** a vytvořte nový obecný deník, který používá název deníku **GenJrn**. Dimenze se ve výchozím nastavení zadávají z názvu deníku (tabulka LedgerJournalName) do hlavičky deníku (tabulka LedgerJournalTable), jak je uvedeno na kartě **Finanční dimenze**.

[![Karta Finanční dimenze na stránce Obecné deníky](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

Jděte na **Řádky**. V poli **Typ účtu** vyberte **Hlavní kniha** a poté do pole **Účet** zadejte **170150**. Poté se z pole přesuňte pomocí klávesy **Tab**. Dimenze se ve výchozím nastavení zadávají z hlavičky deníku. Proto je hodnota **Účet** zobrazena jako **170150-001-024**.

[![Řádky deníku pro obecný deník na stránce poukázky deníku](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

Změňte hodnotu **Účet** na **170150-001-023**. Zadejte částku debetu nebo částku kreditu. V poli **Typ ofsetového účtu** vyberte **Hlavní kniha** a poté do pole **Ofsetový účet** zadejte **600150**. Hodnoty dimenze se ve výchozím nastavení zadávají z účtu. Proto je hodnota **Ofsetový účet** zobrazena jako **600150-001-023**.

### <a name="scenario-2"></a>Scénář 2

Použijte stejné finanční dimenze, které jste definovali pro název deníku ve scénáři 1. Dále přejděte na **Pohledávky \> Zákazníci \> Všichni zákazníci** a definujte výchozí hodnoty finanční dimenze pro zákazníka US-001. Výběrem zákazníka otevřete podrobnosti o zákazníkovi. Na kartě **Finanční dimenze** ponechte výchozí hodnotu pro dimenzi **BUSINESSUNIT** (**001**). Přidejte dimenzi **COSTCENTER** a jako hodnotu zadejte **007**.

Vytvořte nový obecný deník, který používá název deníku **GenJrn**. Na kartě **Finanční dimenze** změňte výchozí hodnotu **BUSINESSUNIT** z **001** na **002**.

Jděte na **Řádky**. V poli **Typ účtu** vyberte **Zákazník** a poté do pole **Účet** zadejte **US-001**. Chcete-li zobrazit finanční dimenze pro typy účtů bez hlavní knihy, vyberte **Finanční dimenze \> Účet**. Pro hodnoty finanční dimenze jsou zadány následující výchozí položky:

- **BUSINESSUNIT:** 002 – Výchozí položka je převzata z hlavičky deníku. Hodnota **001** není ve výchozím nastavení zadána od zákazníka US-001, protože již byla zadána výchozí hodnota.
- **COSTCENTER:** 007 – Výchozí položka je převzata z nastavení zákazníka US-001.
- **DEPARTMENT:** 024 – Výchozí položka je převzata z hlavičky deníku.

Zpátky na řádku v nabídce **Typ ofsetového účtu** vyberte **Hlavní kniha** a poté do pole **Ofsetový účet** zadejte **600150**. Na řádku jsou zadány následující výchozí hodnoty finanční dimenze:

- **BUSINESSUNIT:** 002 – Výchozí položka je převzata z finančních dimenzí účtu. (Ve výchozím nastavení byla původně zadána z hlavičky deníku.)
- **DEPARTMENT:** 024 – Výchozí položka je převzata z finančních dimenzí účtu. (Ve výchozím nastavení byla původně zadána z hlavičky deníku.)
- **COSTCENTER:** 007 – Výchozí položka je převzata z finančních dimenzí účtu. (Ve výchozím nastavení byla původně zadána od zákazníka.)

### <a name="scenario-3"></a>Scénář 3

Do stejného deníku, který jste použili pro scénář 2, přidejte nový řádek. V poli **Typ účtu** vyberte **Hlavní kniha** a poté do pole **Účet** zadejte **170150**. Vymažte výchozí hodnoty dimenze, aby zůstal pouze hlavní účet 170150. V poli **Typ ofsetového účtu** vyberte **Zákazník** a poté do pole **Ofsetový účet** zadejte **US-001**. Pro hodnoty finanční dimenze jsou zadány následující výchozí položky:

- **BUSINESSUNIT:** 002 – Výchozí položka je převzata z hlavičky deníku, protože hodnota dimenze účtu je prázdná. Hodnota **001** není ve výchozím nastavení zadána od zákazníka US-001, protože výchozí hodnota je již převzata z hlavičky deníku. Pokud byla hodnota **BUSINESSUNIT** záměrně ponechána prázdná, musíte také odstranit finanční dimenzi na ofsetovém účtu.
- **COSTCENTER:** 007 – Výchozí položka je převzata ze zákazníka US-001, protože hodnota dimenze účtu a hodnota dimenze hlavičky deníku jsou prázdné. Pokud byla hodnota **COSTCENTER** záměrně ponechána prázdná, musíte také odstranit finanční dimenzi na ofsetovém účtu.
- **DEPARTMENT:** 024 – Výchozí položka je převzata z hlavičky deníku, protože hodnota dimenze účtu je prázdná. Pokud byla hodnota **DEPARTMENT** záměrně ponechána prázdná, musíte také odstranit finanční dimenzi na ofsetovém účtu.

### <a name="scenario-4"></a>Scénář 4

Použijte stejné výchozí hodnoty finanční dimenze, které jste definovali pro název deníku a zákazníka ve scénářích 1 a 2. Dále definujte pevnou hodnotu dimenze pro dimenzi **BUSINESSUNIT** na hlavním účtu 170150. Přejděte na **Hlavní kniha \> Účtová osnova \> Účty \> Hlavní účty**. V poli **Hlavní účet** vyberte **170150** a potom na kartě **Přepisy právnických osob** vyberte **Přidat**. Jako právnickou osobu vyberte **USMF** a poté vyberte **Přidat**. Vyberte tento záznam a poté vyberte **Výchozí dimenze**. Změňte dimenzi **BUSINESSUNIT** na **Pevná hodnota** a jako hodnotu zadejte **003**.

Vytvořte nový obecný deník, který používá název deníku **GenJrn**. Na kartě **Finanční dimenze** odeberte všechny výchozí hodnoty dimenzí.

Jděte na **Řádky**. V poli **Typ účtu** vyberte **Hlavní kniha** a poté do pole **Účet** zadejte **170150**. Poté se z pole přesuňte pomocí klávesy **Tab**. Hodnoty dimenze jsou ve výchozím nastavení zadávány z nastavení hlavního účtu pro účet 170150. Proto je hodnota **Účet** zobrazena jako **170150-003-**.

Změňte hodnotu **Účet** na **170150-004-**. **Funkce deníku nebrání změně hodnoty pevné dimenze.** Zadejte částku debetu nebo částku kreditu. V poli **Typ ofsetového účtu** vyberte **Hlavní kniha** a poté do pole **Ofsetový účet** zadejte **170250**. Hodnota finanční dimenze 004 se ve výchozím nastavení zadává z účtu. Poté dokument zaúčtujte. V deníku vyberte **Poukaz**. Všimněte si, že hodnota **BUSINESSUNIT** byla během účtování vrácena na hodnotu pevné dimenze **003**.

Když se vrátíte k poukazu v deníku, dimenze **BUSINESSUNIT** **neodráží** hodnotu pevného rozměru. Vždy má hodnotu, která byla zobrazena na obrazovce před zaúčtováním. Proces zaúčtování nic nemění na tom, co je uvedeno na poukazu. Během účtování se mění pouze účetní záznam.

## <a name="developer-notes"></a>Poznámky pro vývojáře

Pokud jste vývojář a chcete se podívat na kód pro výchozí proces, zkontrolujte následující metody:

- **LedgerJournalEngine.accountModified()** – Tato metoda je hlavním vstupním bodem procesu výchozího nastavení dimenze primárního účtu, který je standardní pro všechny deníky (a u některých typů deníků je přepsán).
- **LedgerJournalEngine.offsetAccountModified()** – Tato metoda je hlavním vstupním bodem pro výchozí proces dimenze ofsetového účtu.
