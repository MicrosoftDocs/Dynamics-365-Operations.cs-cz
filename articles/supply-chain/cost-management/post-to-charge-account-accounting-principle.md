---
title: Princip účtování na účet poplatků
description: Toto téma poskytuje přehled principu účtování na účet poplatků.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45dc1775c0db83faa89a7a1fa799bdd070d1b09a
ms.sourcegitcommit: 283e237d7bd2a76dd3a8ff64685b0a5f146edd25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/06/2022
ms.locfileid: "8721391"
---
# <a name="post-to-charge-account-accounting-principle"></a>Princip účtování na účet poplatků

Princip účtování *zaúčtovat na účet poplatků* umožňuje zaúčtovat a snadněji odsouhlasit jakékoli rozdíly, které se vyskytnou v jednotkové ceně mezi fyzickým zaúčtováním a finančním zaúčtováním, nepřímé náklady na nakoupené položky nebo poplatky na nákupní objednávce. 

Dvě konfigurace kódů poplatků závazků na stránce **Kód poplatků** (**Závazky \> Nastavení poplatků \> Kód poplatků**) mohou způsobit, že nákupní objednávka ovlivní ocenění inventárních aktiv:

- U kódů poplatků, kde je pole **Typ strany MD** nastaveno na *Položka* a pole **Typ strany Dal** je nastaveno na *Účet hlavní knihy*, funguje účet hlavní knihy vybraný jako absorpční účet coby účet skladových odchylek.
- U kódů poplatků, kde je pole **Typ strany MD** nastaveno na *Položka* a pole **Typ strany Dal** na *Zákazník/Prodejce*, bude náklad účtován jako materiálový náklad a bude použit účet skladových odchylek.

## <a name="european-special-accounting-rule"></a>Evropské zvláštní účetní pravidlo

V Evropě se princip účtování *zaúčtovat na účet poplatků* často používá k začlenění zvláštního účetního pravidla. Například pro zaúčtování změn zásob se obvykle používá jedna z následujících metod:

- **Metoda nákladů na prodej** – Standardní konfigurace profilu účtování zásob tuto metodu podporuje. Princip účtování *zaúčtovat na účet poplatků* není vyžadován.
- **Metoda povahy nákladů** – Tuto metodu často využívají menší organizace. Obvykle zahrnuje následující kroky:

    1. Zboží nebo služby jsou plně zaúčtovány do výdajů v okamžiku přijetí.
    2. Na konci období se provede cyklická inventura.
    3. Ruční úprava množství a hodnoty se zaúčtuje do zásob. (Protiúčet je účet odchylky zásob, který kompenzuje výdaj, který byl zaúčtován v kroku 1. Proto vidíte odchylky v hodnotě zásob pouze na tomto účtu.)

Princip *zaúčtovat na účet poplatků* umožňuje plně automatizovat dvě účtování. Tímto způsobem můžete eliminovat ruční účtování úpravy na konci období.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Aktivace principu zaúčtování na účet poplatků

Chcete-li povolit princip účtování *zaúčtovat na účet poplatků*, postupujte podle těchto kroků.

1. Přejděte do nabídky **Závazky \> Nastavení \> Parametry závazků**.
2. Na kartě **Faktura** na záložce **Faktura** nastavte možnost **Zaúčtovat na účet poplatků v hlavní knize** na *Ano*.
3. Zavřete stránku.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Předpoklady a doporučené parametry pro princip účtování „zaúčtovat na účet poplatků“

Pokud plánujete účtovat nákupní poplatky a skladové odchylky, musí být splněny následující předpoklady:

- Na kartě **Faktura** stránky **Parametry závazků** (**Závazky \> Nastavení \> Parametry závazků**) musí být možnost **Zaúčtovat na účet poplatků v hlavní knize** nastavena na *Ano*.
- Ve stránce **Skupiny modelů položek** (**Řízení nákladů \> Nastavení zásad skladového účetnictví \> Skupiny modelů položek**) musejí být nastaveny všechny následující možnosti na *Ano* pro každou relevantní skupinu modelů, která obsahuje položky zahrnuté v objednávce:

    - Zaúčtovat fyzické zásoby
    - Zaúčtovat finanční zásoby
    - Časově rozlišit pasiva na příjemce produktu

- Na kartě **Dodání** ve stránce **Parametry modulu Zásobování a zdroje** (**Zásobování a zdroje \> Nastavení \> Parametry modulu Zásobování a zdroje**) musí být možnost **Generovat poplatky v příjemce produktu** nastavena na *Ano*.
- Na kartě **Skladové účetnictví** ve stránce **Parametry modulu Řízení zásob a skladu** (**Řízení zásob \> Nastavení \> Parametry modulu Řízení zásob a skladu**) musí být možnost **Zaúčtovat dodací list do hlavní knihy** nastavena na *Ano*.
- Na kartě **Nákupní objednávka** ve stránce **Zaúčtování** (**Řízení zásob \> Nastavení \> Zaúčtování \> Zaúčtování**) musejí být zadány hlavní účty, které se vztahují na každou relevantní položku, pro každý z následujících typů účtování:

    - Nákupní výdaj, bez faktury
    - Nákupní výdaj pro produkt
    - Skladová odchylka

## <a name="example-scenario-1-change-in-unit-cost-price"></a>Příklad scénáře 1: Změna jednotkové nákladové ceny

Tento příklad scénáře má následující předpoklady:

- Nákladový model první do skladu, první ven (FIFO)

Následující postup poskytuje příklad, který ukazuje, co se stane, když změníte jednotkovou cenu v nákupní objednávce.

1. Vytvořte nákupní objednávku pro množství 1 položky, která má a jednotkovou cenu ve výši 100,00.
2. Potvrďte nákupní objednávku.
3. Zaúčtujte příjemku produktu pro nákupní objednávku.
4. Ověřte doklad na příjemce produktu. V následující tabulce vidíte ukázkový doklad.

    | Typ zaúčtování | Hlavní účet | Název hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Fyzická/finanční? | Částka |
    |---|---|---|---|---|---|---|---|
    | Nákup, skladová odchylka | 600170 | Materiály skladové odchylky | Výdaje | Kredit | Číslo | Fyzické | -100,00 |
    | Náklady na nákup přijatého materiálu | 140100 | Zásoby materiálů | Materiál | Debet | Ano | Fyzické | 100.00 |
    | Nákupní výdaj, bez faktury | 600180 | Příjemky materiálů | Výdaje | Debet | Ano | Fyzické | 100.00 |
    | Nákup, časové rozlišení | 200140 | Časově rozlišené nákupy | Pasiva | Kredit | Ano | Fyzické | -100,00 |

5. Zaúčtujte fakturu za nákupní objednávku, která má aktualizovanou jednotkovou cenu 110,00.
6. Ověřte doklad na faktuře. V následující tabulce vidíte ukázkový doklad.

    | Typ zaúčtování | Hlavní účet | Název hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Fyzická/finanční? | Částka |
    |---|---|---|---|---|---|---|---|
    | Nákup, skladová odchylka | 600170 | Materiály skladové odchylky | Výdaje | Kredit | Číslo | Finanční | -10,00 |
    | Náklady na nákup přijatého materiálu | 140100 | Zásoby materiálů | Materiál | Debet | Ano | Finanční | -100,00 |
    | Nákupní výdaj, bez faktury | 600180 | Příjemky materiálů | Výdaje | Debet | Ano | Finanční | -100,00 |
    | Nákup, časové rozlišení | 200140 | Časově rozlišené nákupy | Pasiva | Kredit | Ano | Finanční | 100.00 |
    | Fakturované náklady na nákup materiálu | 140100 | Zásoby materiálů | Materiál | Debet | Číslo | Finanční | 110.00 |
    | Nákupní výdaj pro produkt | 600180 | Příjemka materiálu | Výdaje | Kredit | Číslo | Finanční | 110.00 |
    | Zůstatek dodavatele | 211000 | Obchodní účet závazků | Pasiva | Kredit | Číslo | Finanční | -110,00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>Příklad 2: Poplatky a nepřímé náklady na nákupní objednávce

Tento příklad scénáře má následující předpoklady:

- Nákladový model FIFO
- **Kód poplatků 1:** Debetní položka a účet kreditní knihy pro 10 %
- **Kód poplatků 2:** Debetní položka a zákazník/dodavatel kreditu pro 10,00 proporčně
- **Nepřímé náklady:** 2,00 % připočteno ke kupní ceně

Následující postup poskytuje příklad, který ukazuje, co se stane, když zahrnete poplatky a nepřímé náklady do nákupní objednávky.

1. Vytvořte nákupní objednávku pro množství 1 položky, která má a jednotkovou cenu ve výši 100,00.
2. Přidejte jeden kód poplatků pro 10 procent, které zapíše na vrub položky a připíše k dobru do hlavní knihy.
3. Přidejte jeden kód poplatků pro 10,00, které zapíše na vrub položky a připíše k dobru zákazníka/dodavatele.
4. Přidělte poplatky k řádkům nákupní objednávky.
5. Potvrďte nákupní objednávku.
6. Zaúčtujte příjemku produktu pro nákupní objednávku.
7. Ověřte doklad na příjemce produktu. V následující tabulce vidíte ukázkový doklad.

    | Typ zaúčtování | Hlavní účet | Název hlavního účtu | Typ účtu | Má dáti/Dal? | Clearingový účet | Fyzická nebo finanční | Částka |
    |---|---|---|---|---|---|---|---|
    | Nákup, skladová odchylka | 600170 | Materiály skladové odchylky | Výdaje | Kredit | Číslo | Fyzické | -110,00 |
    | Odhadované absorbované nepřímé náklady | 600520 | Absorbované nepřímé náklady | Výdaje | Kredit | Ano | Fyzické | -2,40 |
    | Dopravné za nákup | 600120 | Dopravné/přepravní náklady | Výdaje | Kredit | Číslo | Fyzické | -10,00 |
    | Náklady na nákup přijatého materiálu | 140100 | Zásoby materiálů | Materiál | Debet | Ano | Fyzické | 122.40 |
    | Nákupní výdaj, bez faktury | 600180 | Příjemky materiálů | Výdaje | Debet | Ano | Fyzické | 110.00 |
    | Nákup, časové rozlišení | 200140 | Časově rozlišené nákupy | Pasiva | Kredit | Ano | Fyzické | -110,00 |

8. Zaúčtujte fakturu pro nákupní objednávku.
9. Ověřte doklad na faktuře. V následující tabulce vidíte ukázkový doklad.

    | Typ zaúčtování | Hlavní účet | Název hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Fyzická/finanční? | Částka |
    |---|---|---|---|---|---|---|---|
    | Nákup, skladová odchylka | 600170 | Materiály skladové odchylky | Výdaje | Kredit | Číslo | Finanční | 0,00 |
    | Odhadované absorbované nepřímé náklady | 600520 | Absorbované nepřímé náklady | Výdaje | Debet | Ano | Finanční | 2.40 |
    | Absorbované nepřímé náklady | 600520 | Absorbované nepřímé náklady | Výdaje | Debet | Číslo | Finanční | -2,40 |
    | Náklady na nákup přijatého materiálu | 140100 | Zásoby materiálů | Materiál | Kredit | Ano | Finanční | -110,00 |
    | Nákupní výdaj, bez faktury | 600180 | Příjemky materiálů | Výdaje | Kredit | Ano | Finanční | -110,00 |
    | Nákup, časové rozlišení | 200140 | Časově rozlišené nákupy | Pasiva | Debet | Ano | Finanční | 110.00 |
    | Fakturované náklady na nákup materiálu | 140100 | Zásoby materiálů | Materiál | Debet | Číslo | Finanční | 110.00 |
    | Nákupní výdaj pro produkt | 600180 | Příjemka materiálu | Výdaje | Kredit | Číslo | Finanční | 110.00 |
    | Zůstatek dodavatele | 211000 | Obchodní účet závazků | Pasiva | Kredit | Číslo | Finanční | -110,00 |
