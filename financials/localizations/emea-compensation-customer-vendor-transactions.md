---
title: "Nastavení kompenzace odběratelů a dodavatelů | Dokumentace společnosti Microsoft"
description: "Toto téma obsahuje informace o tom, jak spustit proces kompenzace účtu odběratele a dodavatele pro právnické osoby, které mají primární adresu v Maďarsku nebo Polsku."
author: mrolecki
manager: AnnBe
ms.date: 05-19-2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: CustTable, CustVendCompensation, VendTable, CustTrans, VendTrans
audience: Application User
ms.reviewer: shylaw
ms.custom: 1691503
ms.search.region: Hungary, Poland
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 716262a2787f312aac758f354a72c7cfd2913dff
ms.openlocfilehash: 4690779974a49d21f21d6df4fc2c8399db9c9e51
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="set-up-customer-and-vendor-compensation"></a>Nastavení kompenzace odběratelů a dodavatelů
Toto téma obsahuje informace, které vám pomohou spustit proces kompenzace pro odběratele a dodavatele, pro právnické osoby, které mají primární adresu v Maďarsku nebo Polsku.

Uživatelé ve východní Evropě musí často vyrovnat částky pohledávek a závazků pro společnost, která je registrována v systému jako odběratel i jako dodavatel. Tento proces vyrovnání používá právní postup, který je označován jako *kompenzace* nebo *čisté bilancování*. 

## <a name="enabling-compensation"></a>Povolení kompenzace

### <a name="set-up-compensation-notes"></a>Nastavení poznámek ke kompenzacím
Můžete nastavit poznámky tak, že budou vytištěny v kompenzačním dopisu. Můžete otevřít stránku **Poznámky na formulářích** z **Nastavení** > **Formuláře** v položkách Pohledávky, Závazky nebo Řízení a účetnictví projektů.

Když vytvoříte novou poznámku na formulář, můžete vybrat část kompenzačního dopisu, pro který nastavujete poznámku:

 - **Kompenzační dopis – záhlaví** – Horní část kompenzačního dopisu, jako je například název společnosti.
 - **Kompenzační dopis – pohledávka** – Tělo kompenzačního dopisu pohledávky.
 - **Kompenzační dopis – závazek** – Tělo kompenzačního dopisu závazku.
 - **Kompenzační dopis – zůstatek** – Tělo kompenzačního dopisu zůstatku.

Můžete zadat poznámku pro každou příslušnou kombinaci poznámky na formuláři a jazyka.

Poznámka na formuláři vychází z matematického znaménka částky zůstatku pro sestavu kompenzace:

- Pokud je částka zůstatku větší než 0 (nula), je vytištěna kompenzační poznámka pohledávky.
- Pokud je částka zůstatku menší než 0 (nula), je vytištěna kompenzační poznámka závazku.
- Pokud je částka zůstatku shodná s kompenzačním dopisem, je vytištěna poznámka zůstatku.

### <a name="set-up-a-vendor-and-a-customer"></a>Nastavení odběratele a dodavatele
Právnická osoba nebo fyzická osoba mohou být odběrateli nebo dodavateli vaší společnosti. Možnost kompenzace je k dispozici pouze pro strany, které jsou přidruženy. Chcete-li nastavit přidružení, otevřete podrobnosti o účtu pro účet odběratele nebo dodavatele a poté na kartě **Různé** ve skupině polí **Úhrady** vyberte účet přidružené strany: **Účet odběratele** pro hlavní data odběratele nebo **Účet dodavatele** pro hlavní data dodavatele.

### <a name="create-a-compensation-journal"></a>Vytvoření deníku kompenzací
Volitelně můžete vytvořit deník, který se použije k představení návrhu kompenzace. Návrh můžete zaúčtovat a také vytisknout sestavu kompenzace. Přejděte do nabídky **Hlavní deník** > **Položky deníku** > **Hlavní deníky**.

## <a name="record-transactions"></a>Záznam transakcí
Obvykle jsou všechny faktury, které jsou zaznamenané pro přidruženého účty odběratelů a dodavatelů, dostupné a kompenzují se jimi: 

 - Prodejní faktury (**Pohledávky** > **Objednávky** > **Všechny prodejní objednávky**)
 - Volné faktury (**Pohledávky** > **Faktury** > **Všechny volné faktury**)
 - Faktury dodavatele (**Závazky** > **Nákupní objednávky** > **Všechny nákupní objednávky**)
 - Projektové prodejní faktury (**Řízení a účetnictví projektů** > **Projektové faktury** > **Návrhy faktury projektu**)

Můžete také použít jakékoliv otevřené transakce dodavatele nebo odběratele v procesu kompenzace. Tyto transakce zahrnují platby nebo faktury, které jsou zaznamenány prostřednictvím deníků. 

## <a name="process-a-compensation-letter"></a>Zpracování kompenzačního dopisu
Pokud máte otevřené transakce dodavatele nebo odběratele, můžete začít proces kompenzace. Otevřete stránku **Všichni odběratelé** nebo **Všichni dodavatelé** a poté klikněte na **Transakce**, abyste zkontrolovali všechny transakce strany. Vyberte jednu nebo více otevřených transakcí (transakce, které mají zůstatek větší nebo menší než 0). Klikněte na tlačítko **Kompenzace** a otevřete stránku **Kompenzace transakcí odběratele/dodavatele**. Tato stránka obsahuje dvě mřížky, jednu pro transakce odběratelů a druhou pro transakce dodavatelů. Jedna z mřížek zobrazí transakce, které jste vybrali. Druhá mřížka zobrazí transakce, které jsou k dispozici pro kompenzaci. Můžete vybrat jednu nebo více transakcí, které chcete označit pro kompenzaci. Po dokončení výběru transakcí klikněte na možnost **Vytvořit kompenzaci**. V zobrazeném dialogovém okně můžete nastavit následující pole:

 - **Deník** – Při vytváření nového deníku vyberte název deníku.
 - **Číslo dávky deníku** – Vyberte stávající číslo dávky deníku.
 - **Datum transakce** – Datum transakce pro položky deníku.
 - **Tisknout sestavu kompenzace** – Tuto možnost vyberte, chcete-li vytisknout sestavu, která bude odeslána vaši spolupracující straně k přijetí.

Pokud nastavíte hodnotu pro pole **Deník** a **Číslo dávky deníku**, číslo má prioritu. Proto se transakce vytvoří v tomto deníku, nikoliv v novém deníku.

## <a name="process-compensation"></a>Zpracování kompenzace
Po vytvoření návrhu kompenzace v deníku a přijetí vašeho návrhu kompenzace vaší spolupracující stranou můžete přejít na hlavní deník a zaúčtovat transakce pro záznam kompenzací do hlavní knihy. Pokud musíte znovu vytisknout sestavu kompenzace, můžete kliknout na **Tisk** > **Kompenzační dopis** na stránce řádků hlavního deníku.


## <a name="frequently-asked-questions"></a>Časté dotazy
**Otázka: Můžu kompenzovat transakce pro více účtů dodavatele a odběratele současně?**

**Odpověď:** Můžete mít vztah úhrad mezi jedním účtem dodavatele a jedním účtem odběratele. Proto můžete zpracovat kompenzaci mezi jednotlivými účty současně.

**Otázka: Mohu použít cizí transakce pro kompenzaci?**

**Odpověď:** Ve výchozím nastavení je funkce kompenzace určena pro transakce v domácí měně. Můžete také použít transakce v cizí měně. V hlavním deníku je však nutné zadat směnný kurz pro transakce návrhu kompenzace, které byly vytvořeny.

**Otázka:: Je funkce kompenzace k dispozici pro všechny země nebo oblasti?**

**Odpověď:** Funkce kompenzace je k dispozici pouze pro právnické osoby, které mají primární adresu v Maďarsku nebo Polsku.

