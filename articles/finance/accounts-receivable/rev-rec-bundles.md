---
title: Sady pro uznání výnosů
description: Toto téma popisuje funkci sady, která je součástí funkce uznání výnosů v pohledávkách. Sada obsahuje nadřazenou položku a několik položek komponent.
author: kweekley
manager: aolson
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: cf4d03c1a697259899c419ce084b35f4eddf13fe
ms.sourcegitcommit: bd53794cb94f8c1ce29a7d6102119a0975f155e3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/09/2021
ms.locfileid: "5142292"
---
# <a name="revenue-recognition-bundles"></a>Sady pro uznání výnosů

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkci sady, která je součástí funkce uznání výnosů v pohledávkách. Sada obsahuje nadřazenou položku a několik položek komponent. Nadřazená položka se nachází na prodejní objednávce, takže je zadání objednávky efektivnější. Poté je však rozbalena do položek komponent. Položky komponent jsou uvedeny v interních dokumentech, například na dodacím listě. Externí dokumenty však obsahují pouze nadřazenou položku.

> [!NOTE]
> Kanály Microsoft Dynamics 365 Commerce, jako je kanál online, pokladní místo (POS) nebo kontaktní středisko, nepodporují uznání výnosů (včetně funkce sady). To platí i pro řešení Zpeněžení potenciálního odběratele pro Dynamics 365 Supply Chain Management a Dynamics 365 Sales. Položky využívající uznání výnosů nesmí být přidány na objednávky nebo do transakcí vytvořených v kanálech Commerce nebo v řešení Zpeněžení potenciálního odběratele.

Sady nastavíte zadáním konfiguračních klíčů pro uznání výnosů. Můžete je však použít i bez nastaveného uznání výnosů. Podobně můžete použít uznání výnosů bez nastavených sad. Je-li nastaveno uznání výnosů, položky komponent určují výnosovou cenu a plán výnosů, které se použijí pro uznání nebo odklad výnosů při fakturaci prodejní objednávky.

Nastavení sad používá funkci kusovníku. Informace o nastavení položky sady najdete v části [Nastavení uznání výnosů](revenue-recognition-setup.md). Pokud je nadřazená položka označena jako sada, bude s ní zacházeno jinak než s ostatními položkami kusovníku. Zde je seznam rozdílů:

- Sady musí být rozbaleny potvrzením prodejní objednávky volbou **Potvrdit prodejní objednávku** na kartě **Prodej** v podokně akcí na stránce prodejní objednávky. Položky sady nesmí být nikdy rozbaleny výběrem položky **Řádek kusovníku** v části **Rozbalení** v nabídce **Řádek prodejní objednávky** na záložce s náhledem **Řádky prodejní objednávky**. V opačném případě bude položka považována za kusovník, a ne za sadu.
- Před vytvořením dodacího listu nebo faktury musí být potvrzena prodejní objednávka, která obsahuje položku sady.
- Když je sada rozbalena potvrzením prodejní objednávky, nadřazená položka je zrušena a její jednotková cena a slevy jsou přiděleny položkám komponent dané sady.
- Součet položek komponent se musí vždy rovnat ceně nadřazené položky. Proto mají pole položek komponent, která lze aktualizovat nebo měnit, jistá omezení. Například nelze ručně změnit jednotkovou cenu. Nelze ji změnit ani nepřímo uplatněním nové cenové smlouvy. Aby se zabránilo nové cenové smlouvě, na položkách komponent nelze změnit dimenze zásob.
- Při tisku externího dokumentu, například potvrzení prodejní objednávky nebo faktury, se vytiskne nadřazená položka místo položek komponent.

## <a name="bundles-on-sales-orders"></a>Sady na prodejních objednávkách

Ukázková společnost USMF používá následující nastavení sady. Všimněte si, že z položek, které jsou součástí tohoto scénáře, bylo odebráno veškeré nastavení uznání výnosů, například nastavení plánů výnosů.

**Nadřazená položka:** Sada Přenosný počítač

- **Položka komponenty:** Množství 1 položky 1000
- **Položka komponenty:** Množství 1 položky S0021
- **Položka komponenty:** Množství 1 položky Podpora

*Základní prodejní cena* pro položky komponent je podstatnou součástí nastavení komponent. Základní prodejní cena je definována na záložce s náhledem **Prodej** příslušné položky. Slouží k výpočtu faktoru přidělení, když je jednotková cena nadřazené položky přidělena k položkám komponent. Za tímto účelem se nikdy nepoužívají prodejní ceny obchodní smlouvy.

Pro položky komponent jsou definovány následující základní prodejní ceny:

- **1000:** $1900
- **S0021:** $150
- **Podpora** $500

Pro odběratele US-004, Cave Wholesales, je zadána prodejní objednávka. Jediný zadaný řádek je pro položku sady Přenosný počítač. Výchozí jednotkovou cenu pro nadřazený řádek lze převzít z mnoha míst, například z obchodní smlouvy nebo základní prodejní ceny. V tomto příkladu byla jako jednotková cena ručně zadána částka $2300.

[![Položka sady Přenosný počítač na prodejní objednávce](./media/bundle-01.png)](./media/bundle-01.png)

Protože prodejní objednávka obsahuje sadu, je nutné ji potvrdit. Dialogové okno pro potvrzení obsahuje komponenty sady.

[![Dialogové okno Potvrzení prodejní objednávky s položkami komponent](./media/bundle-02.png)](./media/bundle-02.png)

Vytištěná sestava o potvrzení však obsahuje pouze nadřazenou položku sady, protože tato sestava je pro odběratele externím dokumentem.

[![Sestava o potvrzení obsahující pouze nadřazenou položku](./media/bundle-03.png)](./media/bundle-03.png)

Po potvrzení prodejní objednávky se v ní stále nachází nadřazená položka, ale její stav je změněn na **Zrušeno**. Čistá částka je navíc sledována v poli **Čistá částka sady**. Tato částka je nutná pro tisk faktury, protože na faktuře je zobrazena nadřazená položka namísto položek komponent.

Součet jednotlivých položek se musí rovnat hodnotě **Čistá částka sady** nadřazené položky, protože tato hodnota je částka, která je odběrateli předložena na vytištěné faktuře. Aby se faktura shodovala s částkami zaúčtovanými do hlavní knihy, úpravy položek komponent jsou omezené. Nelze změnit například pracoviště a sklad, protože tyto změny mohou ovlivnit cenu na obchodní smlouvě.

Jednotková cena na řádku pro nadřazenou položku je přidělena komponentám následujícím způsobem:

**Celkové základní prodejní ceny z komponent:** $1900 + $500 + $150 = $2550

- **Komponenta 1:** $2300 × (1900 ÷ 2550) = $1713,73
- **Komponenta 2:** $2300 USD × (500 ÷ 2550) = $450,98
- **Komponenta 3:** $2300 × (150 ÷ 2550) = $135,29

Součet komponent se musí rovnat $2300, tedy ($1713,73 + $450,98 + $135,29 = $2300).

Pokud je nutné změnit všechny položky komponent, nadřazenou položku lze odebrat. V tomto případě budou odebrány také položky komponent. Nadřazenou položku lze poté znovu přidat a požadované úpravy provést před potvrzením prodejní objednávky.

[![Položka sady obsahující položky komponent](./media/bundle-04.png)](./media/bundle-04.png)

Když je vybrána a zabalena prodejní objednávka, dokumenty obsahují pouze komponenty sady. Součástí dodacího listu a faktury musí být celá sada, jinak je nelze zaúčtovat. Dialogové okno například obsahuje tři položky komponent. Pokud jednu z nich odstraníte, zobrazí se chybová zpráva s oznámením, že všechny produkty v sadě musí být expedovány, než je bude možné fakturovat.

Sada musí být expedována a fakturována jako celý balíček. Pokud například změníte množství položky 1000 na 4, ale ponecháte množství ostatních položek komponent na 5, dodací list a fakturu nebude možné zaúčtovat.

Částečnou částku lze odeslat a fakturovat, pouze pokud je sníženo množství pro všechny komponenty v sadě. Na prodejní objednávce je například zadáno množství 5 pro položku sady Přenosný počítač. Po potvrzení prodejní objednávky bude obsahovat tři položky komponent a množství jednotlivých položek bude 5. Ve výchozím nastavení bude během expedice a fakturace množství nastaveno na 5 pro každou komponentu. U všech tří položek komponent však můžete snížit množství až na 3. V takovém případě budou expedovány a fakturovány tři úplné sady. Zbývající dvě položky sady (množství 2 u každé ze tří položek komponent) lze expedovat a fakturovat později.

Posledním krokem je fakturace prodejní objednávky. Během fakturace se v dialogovém okně faktury zobrazí položky komponent.

[![Dialogové okno Faktura s položkami komponent](./media/bundle-06.png)](./media/bundle-06.png)

Vytištěná faktura však obsahuje pouze nadřazenou položku.
 
[![Vytištěná faktura obsahující pouze nadřazenou položku](./media/bundle-07.png)](./media/bundle-07.png)

Deník faktur, který je vytvořen po zaúčtování, nezahrnuje nadřazenou položku ze sady, protože tato položka je ve stavu **Zrušeno**.

[![Deník faktur, který neobsahuje nadřazenou položku](./media/bundle-08.png)](./media/bundle-08.png)

Je důležité, aby deník faktur nezahrnoval nadřazenou položku ze sady, protože všechny procesy prováděné po zaúčtování faktury jsou založeny na tomto deníku faktur. Pokud například vytvoříte dobropis na kartě **Prodej** v podokně akcí, vytvořený dobropis bude obsahovat položky komponent, ale nebude obsahovat nadřazenou položku.

[![Dobropis obsahující položky komponent, ale ne nadřazenou položku](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]