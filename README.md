# song-collection


@Controller
public class SongController {

    @Autowired
    private GitHubSongRepository gitHubSongRepository;

    @GetMapping("/songs")
    public String listSongs(Model model) {
        List<Song> songs = gitHubSongRepository.getAllSongs();
        model.addAttribute("songs", songs);
        return "song-list";
    }
}



 Spring Cloud Config or Spring Cloud Stream.
