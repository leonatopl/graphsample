# graphsample

library(RColorBrewer)

colourCount = length(unique(pivot_size_plot$Year))
getPalette = colorRampPalette(brewer.pal(9, "Set1"))

ggplot(pivot_size_plot, aes(x = size, y = Freq_size, fill = Year)) +
  geom_bar(stat = "identity", position = "dodge") +
  labs(title = "Frequency by Year", x = "Size", y = "Frequency") +
  scale_fill_manual(values = getPalette(colourCount))

  ![graph](/assets/img/Frequency.GIF)
