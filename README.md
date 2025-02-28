# marketing-strategy
implementing notifications and referral bonus system
// Implementing user engagement notifications and referral bonus system
export const sendNotification = (user, message) => {
    return `Notification sent to ${user.email}: ${message}`;
};

// Function to send financial tips
export const sendFinancialTips = (user) => {
    const tips = [
        'Save at least 20% of your income.',
        'Track your daily expenses.',
        'Invest wisely in low-risk assets.',
        'Avoid impulse purchases.',
        'Review your subscriptions and cancel unused ones.'
    ];
    const randomTip = tips[Math.floor(Math.random() * tips.length)];
    return sendNotification(user, randomTip);
};

// Function to handle referral bonus system
export const handleReferralBonus = (referrer, newUser) => {
    return sendNotification(referrer, `Your friend ${newUser.name} joined BudgetWise! You've earned a $5 referral bonus.`);
};
