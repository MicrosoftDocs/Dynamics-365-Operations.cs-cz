---
title: Vytvoření kódů poplatků
description: Toto téma vysvětluje, jak nakonfigurovat kódy poplatků pro závazky i pohledávky.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8526fa0f3c6e3d1b545703f6e6ef72f558b57bd
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735020"
---
# <a name="create-charges-codes"></a>Vytvoření kódů poplatků

Toto téma vysvětluje, jak nakonfigurovat kódy poplatků pro závazky i pohledávky. Pokud vaše organizace vyžaduje, aby byly kromě řádkových položek v prodejní objednávce nebo objednávce sledovány i částky prodeje nebo částky nákupu, můžete pro tento účel použít kódy poplatků. Například platíte přepravné a pojištění na nákupní objednávce a tyto částky jsou v nákupní objednávce rozepsány samostatně. V tomto případě můžete určit, zda se tyto částky zaúčtují na nákladové účty nebo zda se přidají k pořizovací ceně položek.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Nastavení kódů nákladů pro pohledávky

Chcete-li vytvořit kódy poplatků pro pohledávky, postupujte takto.

1. Přejděte na **Pohledávky** &gt; **Nastavení poplatků** &gt; **Kód poplatků**.
2. Zvolte **Nové**.
3. Zadejte kód pro poplatek do pole **Kód poplatků**.
3. Do pole **Popis** zadejte popis poplatku.
4. Volitelné V poli **Skupina DPH položky** vyberte skupinu DPH.
5. Na pevné záložce **Účtování** zadejte, jak se má poplatek automaticky strhnout a připsat.
6. Pokud jste vybrali **Účet hlavní knihy** jako typ debetu nebo typ kreditu, zadejte typ účtování do polí **Účtování** a zadejte hlavní účet do pole **Účet**.

### <a name="example"></a>Příklad

Váš zákazník platí poplatek. Proto je přidán do součtů prodejní objednávky. Je také nutné nastavit následující informace pro zaúčtování:

- Do pole **Typ** v části **Debetní** vyberte **Zákazník/dodavatel** pro připsání faktury na účet zákazníka.
- V poli **Typ** části **Kredit** vyberte **Účet hlavní knihy**. Poté v poli **Účet** vyberte hlavní účet pro výnosy z poplatků faktury.

> [!NOTE]
> Pokud je pole typ debetu nebo typ kreditu **Účet hlavní knihy** nebo **Položka**, můžete zadat pro transakci poplatku jinou měnu.

Text pro poplatky lze vytisknout v jazyce přiřazeném zákazníkovi. Chcete-li zadat text pro kód poplatků v jiných jazycích, vyberte **Překlady**.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Nastavení kódů poplatků pro závazky

Chcete-li vytvořit kódy poplatků pro závazky, postupujte takto.

1. Proveďte jeden z následujících kroků:

    - Přejděte na **Závazky** &gt; **Nastavení** **poplatků** &gt; **Kód poplatků**.
    - Přejděte na **Zásobování a zajišťování zdrojů** &gt; **Nastavení** &gt; **Poplatky** &gt; **Kód poplatků**.

2. Zvolte **Nové**.
3. Zadejte kód pro poplatek do pole **Kód poplatků**.
3. Do pole **Popis** zadejte popis poplatku.
4. Volitelné V poli **Skupina DPH položky** vyberte skupinu DPH.
5. Volitelné: Do pole **Maximální částka** zadejte maximální částku povolenou pro kód poplatku.

    Toto pole se používá k ověření poplatků za faktury dodavatele. Chcete-li povolit validaci poplatků, zaškrtněte políčko **Povolit ověření párování faktur** na kartě **Ověření faktury** stránky **Parametry závazků**.

    > [!IMPORTANT]
    > Chcete-li ověřit poplatky za faktury, musíte také vytvořit instanci typu pravidla zásady, která je založena na poplatcích pro konkrétní zásady faktury dodavatele.

6. Na pevné záložce **Účtování** zadejte, jak se má poplatek automaticky strhnout a připsat.
7. Pokud jste vybrali **Účet hlavní knihy** jako typ debetu nebo typ kreditu, zadejte typ účtování do polí **Účtování debetu** a **Účtování kreditu** a zadejte hlavní účet do polí **Debetní účet** a **Kreditní účet**.
8. Chcete-li povolit porovnání hodnot poplatků pro fakturu, která obsahuje poplatky z odpovídající hlavičky nebo řádků nákupní objednávky, zaškrtněte políčko **Porovnat hodnoty objednávky a faktury**.

### <a name="example"></a>Příklad

Poplatek můžete zaznamenat jako výdaj jako součást součtu pro nákupní objednávku nebo fakturu dodavatele. K nastavení informací o účtování postupujte následovně. 

- Do pole **Typ** v části **Kreditní** vyberte **Zákazník/dodavatel** pro připsání faktury na účet dodavatele.
- V poli **Typ** části **Debet** vyberte **Účet hlavní knihy**. Poté v poli **Účet** vyberte hlavní účet pro výdaje z poplatků faktury.

Chcete-li nastavit informace o zaúčtování tak, aby se jednotkový poplatek přidal k ceně položky, postupujte podle těchto kroků.

- Do pole **Typ** v části **Kreditní** vyberte **Zákazník/dodavatel** pro připsání faktury na účet dodavatele.
- V poli **Typ** části **Debet** vyberte **Zboží** pro přidání poplatku k ceně zboží.

> [!NOTE]
> Možná budete chtít použít měnu, která se liší od měny uvedené na nákupní objednávce nebo faktuře. Jinou měnu lze zadat v případě, že pro vybraný kód nákladů je typ strany debetu nebo typ kreditu nastaven na možnost **Účet hlavní knihy** nebo **Zboží**.

Text pro poplatky lze vytisknout v jazyce přiřazeném zákazníkovi. Chcete-li zadat text pro kód poplatků v jiných jazycích, vyberte **Překlady**.
